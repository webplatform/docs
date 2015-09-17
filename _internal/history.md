---
title: History
---

<!--
http://jsfiddle.net/renoirb/ts9p2n2n/2/
http://vuejs.org/examples/commits.html
https://github.com/webplatform/mediawiki-conversion/issues/15
-->

<h2 data-history-title>Changes made on </h2>

<div id="history">
    <ul>
        <li v-repeat="commits">
            <a href="{{html_url}}" target="_blank" class="commit">{{sha.slice(0, 7)}}</a> - <span class="message">{{commit.message | truncate}}</span><br \>
            by <span class="author">{{commit.author.name}}</span>
            at <span class="date">{{commit.author.date | formatDate}}</span>
        </li>
    </ul>
</div>
<script>
var apiURL = 'https://api.github.com/repos/webplatform/docs/commits?per_page=20'
  , historyVue = new Vue({
      el: '#history',
      data: {
        branches: ['master', 'manual-edits'],
        currentBranch: 'manual-edits',
        commits: null
      },
      created: function () {
        this.fetchData()
        this.$watch('currentBranch', function () {
          this.fetchData()
        })
      },
      filters: {
        truncate: function (v) {
          var newline = v.indexOf('\n')
          return newline > 0 ? v.slice(0, newline) : v
        },
        formatDate: function (v) {
          return v.replace(/T|Z/g, ' ')
        }
      },
      methods: { 
        fetchData: function () {
          var xhr = new XMLHttpRequest()
            , self = this
            , path = new URL(window.location)
            , validPath = path.searchParams.get('path')
            , translations = ['tr', 'fr', 'pt-br', 'es', 'ja', 'zh', 'de', 'chs', 'ko', 'nl']
            , titleNode = document.querySelectorAll('h2')[0]
            , title = titleNode.innerHTML;
          validPath = validPath
            .replace(/\s+/g, '_')
            .replace(/(\/$)/, '/index') + '.md';
          titleNode.innerHTML = title + ' <em>' + validPath + '</em>';
          apiURL += (!!path.searchParams.get('path'))? '&path=' + validPath :'';
          xhr.open('GET', apiURL + '&sha=' + self.currentBranch)
          xhr.onload = function () {
            self.commits = JSON.parse(xhr.responseText)
          }
          xhr.send()
        }
      }
    });
</script>

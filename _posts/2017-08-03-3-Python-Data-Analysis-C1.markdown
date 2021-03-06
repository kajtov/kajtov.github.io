<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />
<title>Python Data Analysis C1</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>

<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    color: #000 !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.2.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.2.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.2.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.2.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.2.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.2.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=1);
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2);
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=3);
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1);
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1);
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
@media (max-width: 991px) {
  #ipython_notebook {
    margin-left: 10px;
  }
}
[dir="rtl"] #ipython_notebook {
  float: right !important;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#login_widget {
  float: right;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  text-align: center;
  vertical-align: middle;
  display: inline;
  opacity: 0;
  z-index: 2;
  width: 12ex;
  margin-right: -12ex;
}
.alternate_upload .btn-upload {
  height: 22px;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
[dir="rtl"] #tabs li {
  float: right;
}
ul#tabs {
  margin-bottom: 4px;
}
[dir="rtl"] ul#tabs {
  margin-right: 0px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons {
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-right {
  padding-top: 1px;
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-left {
  float: right !important;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: baseline;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
#tree-selector {
  padding-right: 0px;
}
[dir="rtl"] #tree-selector a {
  float: right;
}
#button-select-all {
  min-width: 50px;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
[dir="rtl"] #new-menu {
  text-align: right;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
[dir="rtl"] #running .col-sm-8 {
  float: right !important;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI colors. */
.ansibold {
  font-weight: bold;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  border-left-width: 1px;
  padding-left: 5px;
  background: linear-gradient(to right, transparent -40px, transparent 1px, transparent 1px, transparent 100%);
}
div.cell.jupyter-soft-selected {
  border-left-color: #90CAF9;
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected {
  border-color: #ababab;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 5px, transparent 5px, transparent 100%);
}
@media print {
  div.cell.selected {
    border-color: transparent;
  }
}
div.cell.selected.jupyter-soft-selected {
  border-left-width: 0;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 7px, #E3F2FD 7px, #E3F2FD 100%);
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #66BB6A -40px, #66BB6A 5px, transparent 5px, transparent 100%);
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  padding: 0.4em;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. We need the 0 value because of how we size */
  /* .CodeMirror-lines */
  padding: 0;
  border: 0;
  border-radius: 0;
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul {
  list-style: disc;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ul ul {
  list-style: square;
  margin: 0em 2em;
}
.rendered_html ul ul ul {
  list-style: circle;
  margin: 0em 2em;
}
.rendered_html ol {
  list-style: decimal;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
  margin: 0em 2em;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  background-color: #fff;
  color: #000;
  font-size: 100%;
  padding: 0px;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: 1px solid black;
  border-collapse: collapse;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  border: 1px solid black;
  border-collapse: collapse;
  margin: 1em 2em;
}
.rendered_html td,
.rendered_html th {
  text-align: left;
  vertical-align: middle;
  padding: 4px;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget {
  float: right !important;
  float: right;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  margin-top: 6px;
}
span.save_widget span.filename {
  height: 1em;
  line-height: 1em;
  padding: 3px;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  display: none;
}
.command-shortcut:before {
  content: "(command)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>
<style type="text/css">
    
/* Temporary definitions which will become obsolete with Notebook release 5.0 */
.ansi-black-fg { color: #3E424D; }
.ansi-black-bg { background-color: #3E424D; }
.ansi-black-intense-fg { color: #282C36; }
.ansi-black-intense-bg { background-color: #282C36; }
.ansi-red-fg { color: #E75C58; }
.ansi-red-bg { background-color: #E75C58; }
.ansi-red-intense-fg { color: #B22B31; }
.ansi-red-intense-bg { background-color: #B22B31; }
.ansi-green-fg { color: #00A250; }
.ansi-green-bg { background-color: #00A250; }
.ansi-green-intense-fg { color: #007427; }
.ansi-green-intense-bg { background-color: #007427; }
.ansi-yellow-fg { color: #DDB62B; }
.ansi-yellow-bg { background-color: #DDB62B; }
.ansi-yellow-intense-fg { color: #B27D12; }
.ansi-yellow-intense-bg { background-color: #B27D12; }
.ansi-blue-fg { color: #208FFB; }
.ansi-blue-bg { background-color: #208FFB; }
.ansi-blue-intense-fg { color: #0065CA; }
.ansi-blue-intense-bg { background-color: #0065CA; }
.ansi-magenta-fg { color: #D160C4; }
.ansi-magenta-bg { background-color: #D160C4; }
.ansi-magenta-intense-fg { color: #A03196; }
.ansi-magenta-intense-bg { background-color: #A03196; }
.ansi-cyan-fg { color: #60C6C8; }
.ansi-cyan-bg { background-color: #60C6C8; }
.ansi-cyan-intense-fg { color: #258F8F; }
.ansi-cyan-intense-bg { background-color: #258F8F; }
.ansi-white-fg { color: #C5C1B4; }
.ansi-white-bg { background-color: #C5C1B4; }
.ansi-white-intense-fg { color: #A1A6B2; }
.ansi-white-intense-bg { background-color: #A1A6B2; }

.ansi-bold { font-weight: bold; }

    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}

@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Import packages </span>

<span class="o">%</span><span class="k">matplotlib</span> inline

<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">os</span>

<span class="n">os</span><span class="o">.</span><span class="n">chdir</span><span class="p">(</span><span class="s1">&#39;/Users/kajtova/Spyder/Jupyter&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">style</span><span class="o">.</span><span class="n">use</span><span class="p">(</span><span class="n">os</span><span class="o">.</span><span class="n">path</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">os</span><span class="o">.</span><span class="n">getcwd</span><span class="p">(),</span> <span class="s1">&#39;mystyle.mplstyle&#39;</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[2]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Two dataframes exist in the example, ratings and movies. </span>
<span class="c1"># Goal: check the distribution of rating of drama movies. Movies database has no information on the genre of the movie, instead the two dataframes can be matched through item id. </span>

<span class="n">column_names</span> <span class="o">=</span> <span class="p">[</span> <span class="s1">&#39;user id&#39;</span><span class="p">,</span> <span class="s1">&#39;item id&#39;</span><span class="p">,</span> <span class="s1">&#39;rating&#39;</span><span class="p">,</span> <span class="s1">&#39;timestamp&#39;</span> <span class="p">]</span>

<span class="n">ratings</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span> <span class="s1">&#39;ratings.dat&#39;</span><span class="p">,</span> <span class="n">sep</span> <span class="o">=</span> <span class="s1">&#39;::&#39;</span><span class="p">,</span> <span class="n">index_col</span> <span class="o">=</span> <span class="kc">False</span><span class="p">,</span> <span class="n">names</span> <span class="o">=</span> <span class="n">column_names</span><span class="p">,</span> <span class="n">encoding</span> <span class="o">=</span> <span class="s2">&quot;UTF-8&quot;</span><span class="p">,</span> <span class="n">engine</span> <span class="o">=</span> <span class="s1">&#39;python&#39;</span> <span class="p">)</span>

<span class="c1"># Preivew the data</span>
<span class="n">ratings</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
<span class="n">ratings</span><span class="o">.</span><span class="n">tail</span><span class="p">()</span>
<span class="n">ratings</span><span class="p">[</span><span class="mi">1</span><span class="p">:</span><span class="mi">2</span><span class="p">]</span>
<span class="n">ratings</span><span class="p">[:</span><span class="mi">5</span><span class="p">]</span>

<span class="c1"># Calculate the frequency of [&#39;rating&#39;], sort the result and plot a bar:</span>
<span class="n">ratings_counts</span> <span class="o">=</span> <span class="n">ratings</span><span class="p">[</span><span class="s1">&#39;rating&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">value_counts</span><span class="p">()</span>
<span class="n">ratings_counts_sorted</span> <span class="o">=</span> <span class="n">ratings_counts</span><span class="o">.</span><span class="n">sort_index</span><span class="p">()</span>
<span class="n">ratings_counts_sorted</span><span class="o">.</span><span class="n">plot</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span> <span class="n">color</span> <span class="o">=</span> <span class="s1">&#39;Blue&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span> <span class="s1">&#39;Movie rating&#39;</span> <span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span> <span class="s1">&#39;Rating&#39;</span> <span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span> <span class="s1">&#39;Count&#39;</span> <span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt output_prompt">Out[2]:</div>



<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.text.Text at 0x11ad0d198&gt;</pre>
</div>

</div>

<div class="output_area">
<div class="prompt"></div>



<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAjMAAAF+CAYAAAB3fJvtAAAABHNCSVQICAgIfAhkiAAAAAlwSFlz
AAAPYQAAD2EBqD+naQAAIABJREFUeJzs3XtUVPX+P/7nMAwMI8jFUZSUyIOgoJZl4gU+9IHxIF6D
vGCmmZ2UwETrdMzPx3M0j57U5cmcjhdOmfoByw6irsLQFBXRlZqGGpKQhqlpwkhcZYZhZv/+6Df7
63a4iShsfT7WYuG892u/5zV7lfN07/fsUQiCIICIiIhIphzaugEiIiKie8EwQ0RERLLGMENERESy
xjBDREREssYwQ0RERLLGMENERESyxjBDREREssYwQ0RERLLGMENERESyxjBDRI8MhUKBXbt2tXUb
os2bN8PDw6Ot2yCSPYYZImoT06dPh0KhQHx8vN22xMREKBQKTJ8+vVWf8/r164iOjm7VOZvLz88P
H3zwgWRs0qRJKCwsbJN+iB4mDDNE1GZ69OiBbdu2oaamRhwzGo349NNP4evr2+rP17VrVzg7O7fa
fIIgoK6ursX7u7i4oEuXLq3WD9GjimGGiNrM008/jR49emDHjh3i2I4dO+Dr64sBAwZIak0mE+bM
mYMuXbpArVYjNDQU3377LQDAarWie/fuWL9+vWSf3NxcODg44OeffwZgf5npypUrmDhxIjw8PODl
5YVx48bh0qVLDfZ76NAhKBQKZGZm4plnnoGzszOOHDmCixcvYty4cfD29oarqyueffZZ7N+/X9zv
ueeew88//4x58+ZBoVBAoVAAsL/MtHjxYjz11FNISUmBn58f3N3dERcXh8rKSrGmsrISU6ZMQYcO
HfDYY49Br9fjueeew9y5c5t72IkeOgwzRNSmZsyYgU2bNomPP/nkE7zyyit2dX/5y1+Qnp6OLVu2
4LvvvoO/vz+ioqJQWloKBwcHTJ48GZ9++qlkn61bt2LYsGF4/PHH7eYzm82IioqCm5sbcnJycPTo
Ubi6umLEiBGora1ttOd33nkHy5cvxw8//ID+/fujqqoKI0eORFZWFnJzczFixAiMGTMGly9fBvB7
QOvevTuWLFmC69ev4/r16w3OffHiRezatQsZGRnIyMhAdnY2li9fLm5/8803cfToUXzxxRfYu3cv
Dh06hNzc3Eb7JXroCUREbeDll18Wxo0bJxQXFwvOzs7CpUuXhEuXLglqtVooKSkRxo0bJ7z88suC
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
++KLL+Dm5oaVK1ciLy8PJSUlsFqt6N69O6KjozF16tR6P720c+dOyXczTZw4EZMnT7b7yHRFRQXW
rFmDQ4cOwWQyISgoCHPnzrW7pwwAnD59Gnq9HgUFBdBoNNDpdJg9ezY6dOggqbNardiyZQt27NgB
g8GAHj164JVXXkF0dPQ9HKXfxcfHi+uBNmzYcM/zERE9DHgHYHlpjfeydhdmqPkYZoiI7DHMyEtr
vJfJbs0MERER0e0YZoiIiEjWGGaIiIhI1hhmiIiISNYYZoiIiEjWGGaIiIhI1hhmiIiISNba3R2A
iYio/WvNe7nwPi50r3hmhoiIiGSNYYaIiIhkjWGGiIiIZI1hhoiIiGSNYYaIiIhkjWGGiIiIZI1h
hoiIiGSNYYaIiIhkjWGGiIiIZI1hhoiIiGSNYYaIiIhkjWGGiIiIZI1hhoiIiGSNYYaIiIhkjWGG
iIiIZI1hhoiIiGSNYYaIiIhkjWGGiIiIZI1hhoiIiGSNYYaIiIhkjWGGiIiIZI1hhoiIiGSNYYaI
iIhkzbGtG7jdrVu3kJKSgry8PJw7dw4VFRVYtGgRxowZI9ZYrVbs3r0bBw4cQGFhIcrLy+Hj44M/
/vGPmDp1KpydnSVzDhw4sN7nmj17NqZPny4Zq6yshF6vx8GDB2E0GhEcHIx58+ahd+/edvufOXMG
er0e58+fh6urK3Q6HRITE6HRaCR1VqsVKSkpSE9Ph8FggK+vL6ZPn44RI0a08CgRERHR7dpVmCkr
K8NHH32Erl27olevXjh16pRdjdFoxLvvvot+/fohNjYWXl5eOHv2LP7973/j22+/xYYNG6BQKCT7
hISEYNSoUZKxwMBAyWOr1YqkpCT8+OOPmDp1Kjw8PLB9+3bMmjULKSkp8PX1FWsLCgqQkJAAPz8/
zJs3D8XFxUhNTcWVK1eg1+sl865btw6bN29GTEwMgoKCkJ2djYULF0KhUCAqKupeDxkREdEjr12F
Ga1Wiz179kCr1SI/Px/Tpk2zq1GpVNi4cSOefPJJcSwmJgY+Pj5ITk7GiRMnEBISItnH19cXI0eO
bPS5s7KycPbsWSxfvhw6nQ4AMHz4cMTGxiI5ORnLli0Ta9euXQs3NzckJyfD1dUVAODj44OlS5fi
2LFjGDx4MACIIWfChAmYP38+AOD555/HzJkzodfrodPpoFQqW3CkiIiIyKZdrZlxcnKCVqtttEal
UkmCjM1///d/AwCKiorq3c9oNMJkMjU4b1ZWFjp16oSIiAhxzNPTEzqdDtnZ2aitrQUAVFVV4fjx
44iOjhaDDACMGjUKGo0G+/btE8eys7NRV1eHCRMmiGMKhQIvvPACbty4ge+//77Bfmpqapr8sVgs
De5PRET0qGhXZ2buhcFgAAB4eHjYbcvIyMD27dshCAKeeOIJvPrqq3ZrVgoKChAYGAgHB2m+Cw4O
xs6dO3H58mX4+/vjwoULsFgsCAoKktSpVCoEBASgoKBAMqeLiwueeOIJSW3fvn0BAOfPn8dTTz1V
7+sJCwtr1uvu2bNns+qIiIgeVg9NmPm///s/dOjQAcOGDZOM9+/fH8OHD4ePjw9KSkqQlpaGhQsX
oqqqCuPHjxfrDAYDBgwYYDev7UxRSUkJ/P39xdBU3xkkrVaL3NxcyZxeXl52a3hs+9rmIiIiopZ7
KMLMJ598ghMnTuCdd96Bm5ub3bbbjRs3Di+99BLWrl2L0aNHQ61WAwBMJhOcnJzs5rZ9Osp2icr2
W6VS2dU6OTlJLmU1NKdtrLHLXjk5OQ1us5kzZw7Ky8ubrCMiInqYtas1My3x9ddfY/369Rg3bpzk
TEtDVCoVJk6ciMrKSpw/f14cd3Z2FtfF3M4WOGyhxvbbbDbb1dbW1ko+Gt7QnLaxOz9GfjsXF5cm
f7h4mIiISOZh5tixY1i0aBFCQ0OxYMGCZu/n7e0NAJKzGlqttt7LPraxzp07i3W3j99Za6uz1d68
eROCINQ7Z1OLnYmIiKhpsg0zeXl5ePvtt9GnTx+89957cHRs/hWzX375BcDvn1aysS3etVqtktpz
585BrVaL95nx9/eHUqlEfn6+pM5sNqOwsBABAQGSOY1Go90nrPLy8gDY3+uGiIiI7p4sw0xRURGS
kpLQrVs3fPDBB+K6lzv99ttvdmPV1dX47LPP4OHhgT59+ojjkZGRuHnzJg4cOCCOlZWVYf/+/QgL
CxPXubi6uiIkJASZmZmorq4Wa3fv3o1bt26J96gBgPDwcDg6OiItLU0cEwQB6enp6NKlC/r379/y
g0BEREQA2uEC4M8//xyVlZXipZjDhw/jxo0bAIC4uDgoFArMnj0blZWVmDp1Ko4cOSLZv3v37mJI
+M9//oPs7GyEhYWha9euMBgM+OKLL/Drr79iyZIlkkW8kZGR6NevH5YsWYKioiJ4eHggLS0NVqsV
s2bNkjxHQkICZsyYgZkzZyImJgbFxcXYunUrBg8ejKFDh4p13t7emDx5MlJSUlBXV4fg4GAcOnQI
ubm5WLp0Kde8EBERtQKFcOeCjjY2ZswYXL9+vd5tX3zxBQBg7NixDe4/evRoLF68GMDva2pSUlJw
4cIFlJeXw8XFBcHBwXj55Zfx7LPP2u1bUVGBNWvW4NChQzCZTAgKCsLcuXPt7ikDAKdPn4Zer0dB
QQE0Gg10Oh1mz56NDh06SOqsViu2bNmCHTt2wGAwoEePHnjllVcQHR3d3EPSoPj4eJSWlsLLywsb
Nmy45/mIiJrrjjtO3JPWfhdqzd6A1u+PpFrjvazdhRlqPoYZImorDDPUWlrjvUyWa2aIiIiIbBhm
iIiISNYYZoiIiEjWGGaIiIhI1hhmiIiISNYYZoiIiEjWGGaIiIhI1hhmiIiISNYYZoiIiEjWGGaI
iIhI1hhmiIiISNYYZoiIiEjWGGaIiIhI1hhmiIiISNYYZoiIiEjWGGaIiIhI1hhmiIiISNYYZoiI
iEjWGGaIiIhI1hhmiIiISNYYZoiIiEjWGGaIiIhI1hhmiIiISNYYZoiIiEjWGGaIiIhI1hhmiIiI
SNYYZoiIiEjWGGaIiIhI1hhmiIiISNYYZoiIiEjWHNu6gdvdunULKSkpyMvLw7lz51BRUYFFixZh
zJgxdrVFRUV4//33cfr0aahUKgwbNgxvvvkmPD097Wp37dqF1NRUXLt2Dd7e3pg0aRLi4uLs6ior
K6HX63Hw4EEYjUYEBwdj3rx56N27t13tmTNnoNfrcf78ebi6ukKn0yExMREajUZSZ7VakZKSgvT0
dBgMBvj6+mL69OkYMWLEPRwpIiIismlXZ2bKysrw0UcfoaioCL169Wqw7saNG3jttddw5coVJCYm
4qWXXsLRo0eRmJgIs9ksqU1PT8fSpUvRs2dPvP322+jXrx9WrVqFzZs3S+qsViuSkpKwZ88eTJw4
EXPmzMFvv/2GWbNm4fLly5LagoICJCQkwGg0Yt68eRg3bhx27tyJd955x67XdevW4cMPP0RISAje
fvttdO3aFQsXLsTevXtbfqCIiIhI1K7OzGi1WuzZswdarRb5+fmYNm1avXWbNm1CTU0NUlNT0bVr
VwBAcHAwEhMT8eWXXyI2NhYAYDQasW7dOoSGhmLlypUAgJiYGAiCgI0bNyI2NhYdO3YEAGRlZeHs
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
Rffu3ZGYmIipU6fa3SdmwoQJcHR0RGpqKg4fPgxvb2+8+eabmDx5sqROqVRizZo1WLNmDbZt2waT
yYSgoCAsXrxYDE02vXv3xrp166DX67F69WpoNBqMHTvW7lNWRERE1DIKQRCE5hZv27YNer0e//nP
f9C9e/cG665evYqJEyciKSkJkyZNapVGyV58fDxKS0vh5eWFDRs2tHU7RNSKWnu9QfP/pm+e1uyv
PfcGtO/+2nNvQPP6a433srtaALxv3z5EREQ0GmQAoHv37oiMjMTevXtb1BQRERFRc91VmLlw4QKe
euqpZtU++eSTuHjxYouaIiIiImquuwozdXV1zf6uJUdHxwZvQkdERETUWu4qzGi12mafbbl48WK9
30lERERE1JruKswMGjQIX331ld1dcu9k+16mkJCQe2qOiIiIqCl3FWZefvllmEwmxMfHIy8vr96a
vLw8vP766zCZTJg2bVqrNElERETUkLu6z0z37t2xfPly/O///i9mzJiBxx57DP7+/tBoNLh16xYu
XryIq1evQq1W4x//+EeTn3oiIiIiuld3fQfg0NBQfPbZZ9iyZQuOHDmCQ4cOids6d+6M559/HtOm
TWOQISIiogeiRV9n4OPjgwULFgD4/Usbq6ur0aFDB7vvQCIiIiK631r83Uw2DDFERETUlu5qATAR
ERFRe8MwQ0RERLLGMENERESyxjBDREREssYwQ0RERLLGMENERESyxjBDREREssYwQ0RERLLGMENE
RESyxjBDREREssYwQ0RERLLGMENERESyxjBDREREssYwQ0RERLLGMENERESyxjBDREREssYwQ0RE
RLLGMENERESyxjBDREREssYwQ0RERLLm2NYNtMTJkycRHx9f77ZNmzahX79+4uOioiK8//77OH36
NFQqFYYNG4Y333wTnp6edvvu2rULqampuHbtGry9vTFp0iTExcXZ1VVWVkKv1+PgwYMwGo0IDg7G
vHnz0Lt3b7vaM2fOQK/X4/z583B1dYVOp0NiYiI0Gs09HAEiIiKykWWYsYmLi0NQUJBkrEePHuKf
b9y4gddeew2urq5ITEzErVu3kJqaiosXL2LLli1QqVRibXp6Ot577z1ERERgypQpyM3NxapVq2A0
GjF9+nSxzmq1IikpCT/++COmTp0KDw8PbN++HbNmzUJKSgp8fX3F2oKCAiQkJMDPzw/z5s1DcXEx
UlNTceXKFej1+vt3YIiIiB4hsg4zTz31FHQ6XYPbN23ahJqaGqSmpqJr164AgODgYCQmJuLLL79E
bGwsAMBoNGLdunUIDQ3FypUrAQAxMTEQBAEbN25EbGwsOnbsCADIysrC2bNnsXz5cvG5hw8fjtjY
WCQnJ2PZsmXi869duxZubm5ITk6Gq6srAMDHxwdLly7FsWPHMHjw4NY/KERERI8Y2a+Zqa6uRl1d
Xb3bDhw4gLCwMDHIAEBISAh8fX2xf/9+cezkyZMoLy/H+PHjJftPmDABNTU1OHLkiDiWlZWFTp06
ISIiQhzz9PSETqdDdnY2amtrAQBVVVU4fvw4oqOjxSADAKNGjYJGo8G+ffvu7YUTERERAJmHmSVL
liA8PBzDhg3DrFmzkJ+fL24rLi5GaWkp+vTpY7dfcHAwCgoKxMe2P995yapPnz5wcHCwqw0MDISD
g/TQBQcHw2g04vLlywCACxcuwGKx2M2pUqkQEBAgmbM+NTU1Tf5YLJZG5yAiInoUyPIyk0qlQkRE
BIYNGwYPDw8UFRUhJSUFr732GjZu3IjevXvDYDAAALRard3+Wq0W5eXlqK2thZOTEwwGA5RKJby8
vOyex93dHSUlJeKYwWDAgAED6p0TAEpKSuDv79/k8+fm5jb6GsPCwpo4Cr/r2bNns+qIiIgeVrIM
M08++SSefPJJ8XF4eDgiIyMRFxeHtWvX4sMPP4TJZAIAODk52e3v7OwMADCZTHBycoLJZIKjY/2H
wrbdxrZPY3Pe/vv2RcYNzUlEREQtJ8swU58ePXogPDwcBw8ehMViEcOFbQ3L7WxBwlbj7Ozc4Lqb
2tpasc5W29w5AcBsNjc5Z31ycnIa3Q4Ac+bMQXl5eZN1RERED7OHJswAgLe3N8xmM2pqasTLO7bL
PbczGAxwd3cXz7BotVpYLBaUlpZKLjWZzWaUl5ejc+fO4phWq21wTgBibVPPf/uc9XFxcWl0OwAo
lcoma4iIiB52sl4AfKdffvkFzs7O0Gg06NKlCzw9PfHDDz/Y1Z07dw4BAQHi48DAQACQLCC2PbZa
rZJa2+Jdq9VqN6darRbvM+Pv7w+lUmk3p9lsRmFhoWROIiIiajlZhpnffvvNbqywsBCHDx9GSEiI
+EmjiIgI5OTk4NdffxXrTpw4gcuXLyMyMlIcGzhwINzd3ZGeni6Zc/v27VCr1QgNDRXHIiMjcfPm
TRw4cEAcKysrw/79+xEWFiae7XF1dUVISAgyMzNRXV0t1u7evRu3bt1q9P44RERE1HyyvMy0YMEC
ODs7o3///vDy8sJPP/2EnTt3Qq1W44033hDrXnnlFezfvx/x8fGIi4tDTU0NUlJS4O/vj7Fjx4p1
arUa8fHxWLFiBebPn48hQ4YgNzcXmZmZSEhIgLu7u1gbGRmJfv36YcmSJSgqKoKHhwfS0tJgtVox
a9YsSZ8JCQmYMWMGZs6ciZiYGBQXF2Pr1q0YPHgwhg4dev8PFBER0SNAIQiC0NZN3K1t27YhMzMT
V69eRVVVFTw9PfHss89i5syZkq8zAICLFy9i9erV4nczhYaGYu7cuejUqZPdvDt37pR8N9PEiRMx
efJkKBQKSV1FRQXWrFmDQ4cOwWQyISgoCHPnzrW7pwwAnD59Gnq9HgUFBdBoNNDpdJg9ezY6dOhw
z8chPj5eXOezYcOGe56PiNqPO/7auWet/Td9a/bXnnsD2nd/7bk3oHn9tcZ7mSzDDP2OYYbo3vBN
peV47FqOx06qNd7LZLlmhoiIiMiGYYaIiIhkjWGGiIiIZI1hhoiIiGSNYYaIiIhkjWGGiIiIZI1h
hoiIiGSNYYaIiIhkjWGGiIiIZI1hhoiIiGSNYYaIiIhkjWGGiIiIZI1hhoiIiGSNYYaIiIhkjWGG
iIiIZI1hhoiIiGSNYYaIiIhkjWGGiIiIZI1hhoiIiGSNYYaIiIhkjWGGiIiIZI1hhoiIiGSNYYaI
iIhkjWGGiIiIZI1hhoiIiGSNYYaIiIhkjWGGiIiIZI1hhoiIiGSNYYaIiIhkjWGGiIiIZI1hhoiI
iGTNsa0baIlz584hIyMDp06dwrVr1+Du7o5+/frh9ddfx+OPPy7WLV68GBkZGXb7P/7440hPT7cb
37VrF1JTU3Ht2jV4e3tj0qRJiIuLs6urrKyEXq/HwYMHYTQaERwcjHnz5qF37952tWfOnIFer8f5
8+fh6uoKnU6HxMREaDSaezwKREREBMg0zGzZsgVnzpyBTqdDr169YDAYkJaWhpdeegmbNm2Cv7+/
WOvk5ISFCxdK9nd1dbWbMz09He+99x4iIiIwZcoU5ObmYtWqVTAajZg+fbpYZ7VakZSUhB9//BFT
p06Fh4cHtm/fjlmzZiElJQW+vr5ibUFBARISEuDn54d58+ahuLgYqampuHLlCvR6fesfGCIiokeQ
LMPMlClTsGzZMqhUKnHsj3/8I+Li4rBlyxb8/e9/F8eVSiVGjhzZ6HxGoxHr1q1DaGgoVq5cCQCI
iYmBIAjYuHEjYmNj0bFjRwBAVlYWzp49i+XLl0On0wEAhg8fjtjYWCQnJ2PZsmXivGvXroWbmxuS
k5PFAOXj44OlS5fi2LFjGDx4cOscECIiokeYLNfMPPnkk5IgAwC+vr7o2bMnioqK7OotFguqqqoa
nO/kyZMoLy/H+PHjJeMTJkxATU0Njhw5Io5lZWWhU6dOiIiIEMc8PT2h0+mQnZ2N2tpaAEBVVRWO
Hz+O6OhoyZmgUaNGQaPRYN++fY2+xpqamiZ/LBZLo3MQERE9CmR5ZqY+giCgtLQUPXv2lIwbjUaE
h4fDaDSiY8eOiIqKwhtvvCFZs1JQUAAACAoKkuzbp08fODg4oKCgQDy7U1BQgMDAQDg4SHNgcHAw
du7cicuXL8Pf3x8XLlyAxWKxm1OlUiEgIEB8zoaEhYU163Xf+XqJiIgeNQ9NmMnMzERxcTFmzZol
jmm1WkybNg29e/eG1WrFN998g7S0NBQWFiI5ORmOjr+/fIPBAKVSCS8vL8mcKpUK7u7uKCkpEccM
BgMGDBhg9/xarRYAUFJSAn9/fxgMBsn4nbW5ubn3/qKJiIjo4Qgzly5dwooVK9C/f3+MHj1aHJ89
e7akLioqCr6+vli3bh2ysrIQFRUFADCZTGKwuZOTkxNMJpP42GQywcnJya7O2dlZ3H777zsvh9U3
Z31ycnIa3Q4Ac+bMQXl5eZN1REREDzNZrpm5ncFgQFJSElxdXbFixQoolcpG61988UU4ODjgxIkT
4pizszPq6urqra+trRWDiq3Wti7mdrZwYqu1/TabzU3OWR8XF5cmf5p6rURERI8CWYeZqqoqzJkz
B1VVVfjwww/RuXPnJvdRq9Vwd3dHRUWFOKbVamGxWFBaWiqpNZvNKC8vl8yr1WrFS0i3s43Zam2X
lxqqbU6vRERE1DTZhhmTyYR58+bh8uXLWL16dbMXwlZXV6OsrAweHh7iWGBgIAAgPz9fUpufnw+r
1YqAgABxzLZ412q1SmrPnTsHtVot3mfG398fSqXSbk6z2YzCwkLJnERERNRysgwzFosFCxYsEO/3
0r9/f7sak8mE6upqu/GPP/4YgiBg6NCh4tjAgQPh7u5ud1fg7du3Q61WIzQ0VByLjIzEzZs3ceDA
AXGsrKwM+/fvR1hYmLiextXVFSEhIcjMzJT0sXv3bty6dUu8Rw0RERHdG1kuAP7ggw9w+PBhhIWF
oaKiAl999ZVk+8iRI3Hz5k1MmTIFUVFR8PPzAwB88803OHr0KIYOHYrw8HCxXq1WIz4+HitWrMD8
+fMxZMgQ5ObmIjMzEwkJCXB3dxdrIyMj0a9fPyxZsgRFRUXw8PBAWloarFar5JNUAJCQkIAZM2Zg
5syZiImJQXFxMbZu3YrBgwdLwhQRERG1nCzDjO0eLTk5OfV+6mfkyJFwc3NDaGgojh8/joyMDFit
VnTv3h2JiYmYOnWq3X1iJkyYAEdHR6SmpuLw4cPw9vbGm2++icmTJ0vqlEol1qxZgzVr1mDbtm0w
mUwICgrC4sWLxdBk07t3b6xbtw56vR6rV6+GRqPB2LFj7T5lRURERC2nEARBaOsmqGXi4+NRWloK
Ly8vbNiwoa3bIZIdhaL15mrtv0lbszegfffXnnsD2nd/7bk3oHn9tcZ7mSzPzBCRPLT3NxUiejjI
cgEwERERkQ3DDBEREckawwwRERHJGsMMERERyRrDDBEREckawwwRERHJGsMMERERyRrDDBEREcka
wwwRERHJGsMMERERyRrDDBEREckawwwRERHJGsMMERERyRrDDBEREckawwwRERHJmmNbN0BELadQ
tO58gtC68xERPQg8M0NERESyxjBDREREssYwQ0RERLLGMENERESyxjBDREREssZPM1Gb4ydyiIjo
XvDMDBEREckaz8wQNYFnjoiI2jeemSEiIiJZY5ghIiIiWWOYISIiIlljmCEiIiJZY5ghIiIiWeOn
mR6A2tpabNiwAV999RUqKyvh7++P119/HYMHD27r1oiIiGSPZ2YegMWLF2Pr1q2Ijo7GW2+9BaVS
iaSkJJw+fbqtWyMiIpI9hpn7LC8vD19//TVmz56NpKQkxMbGYv369ejWrRv0en1bt0dERCR7DDP3
WVZWFpRKJWJiYsQxZ2dnjBs3DmfPnsWvv/7aht0RERHJH9fM3GcFBQXw9fWFq6urZDw4OBgAUFhY
iK5du9rtV1NT0+TcFouldZokIiKSMYUg8Obq99PEiRPRqVMnrF+/XjL+008/YeLEiViwYAFeeOEF
u/0GDhzYrPl79uwJhUIBT0/PRuuuXm1+z83RvXvrzdWeewPad3/tuTfg0eqvPfcGtO/+2nNvQPvu
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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Filtering data based on a condition</span>
<span class="n">column_names</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;movies id&#39;</span><span class="p">,</span> <span class="s1">&#39;movie title&#39;</span><span class="p">,</span> <span class="s1">&#39;genre&#39;</span> <span class="p">]</span>

<span class="n">movies</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span> <span class="s1">&#39;movies.dat&#39;</span><span class="p">,</span> <span class="n">sep</span> <span class="o">=</span> <span class="s1">&#39;::&#39;</span><span class="p">,</span> <span class="n">names</span> <span class="o">=</span> <span class="n">column_names</span><span class="p">,</span> <span class="n">index_col</span> <span class="o">=</span> <span class="kc">False</span><span class="p">,</span> <span class="n">encoding</span> <span class="o">=</span> <span class="s1">&#39;UTF-8&#39;</span><span class="p">,</span> <span class="n">engine</span> <span class="o">=</span> <span class="s1">&#39;python&#39;</span> <span class="p">)</span>

<span class="n">movies</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>

<span class="n">movies</span><span class="o">.</span><span class="n">genre</span><span class="o">.</span><span class="n">unique</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt output_prompt">Out[3]:</div>



<div class="output_text output_subarea output_execute_result">
<pre>array([&#39;Documentary|Short&#39;, nan, &#39;Short|Horror&#39;, ...,
       &#39;Documentary|Animation|Mystery&#39;, &#39;Comedy|Talk-Show&#39;,
       &#39;Documentary|Crime|Sport&#39;], dtype=object)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Create new dataframe, which is a subset of the movies dataframe, conditional on the genre</span>

<span class="n">movies_drama</span> <span class="o">=</span> <span class="n">movies</span><span class="p">[</span><span class="n">movies</span><span class="p">[</span><span class="s1">&#39;genre&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Crime|Drama&#39;</span> <span class="p">]</span>

<span class="n">movies_drama_row</span> <span class="o">=</span> <span class="n">movies_drama</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="c1"># gives number of row count</span>
<span class="n">movies_drama_col</span> <span class="o">=</span> <span class="n">movies_drama</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="c1"># gives number of col count</span>
<span class="nb">print</span><span class="p">(</span> <span class="n">movies_drama_row</span><span class="p">,</span> <span class="n">movies_drama_col</span> <span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>

<div class="output_subarea output_stream output_stdout output_text">
<pre>342 3
</pre>
</div>
</div>

<div class="output_area">
<div class="prompt output_prompt">Out[4]:</div>



<div class="output_text output_subarea output_execute_result">
<pre>15      2844
216    20859
230    21406
262    22286
265    22403
Name: movies id, dtype: int64</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Select only the ids form the drama movies, and based on these ids, check if they appear in the movies dataframe</span>

<span class="n">movies_drama_id</span> <span class="o">=</span> <span class="n">movies_drama</span><span class="p">[</span> <span class="s1">&#39;movies id&#39;</span> <span class="p">]</span>
<span class="n">movies_drama_id</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>

<span class="c1"># Extract the ids in the ratings that correspond to drama movies</span>
<span class="n">criterion</span> <span class="o">=</span> <span class="n">ratings</span><span class="p">[</span><span class="s1">&#39;item id&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">map</span><span class="p">(</span> <span class="k">lambda</span> <span class="n">x</span><span class="p">:(</span> <span class="n">movies_drama_id</span> <span class="o">==</span> <span class="n">x</span> <span class="p">)</span><span class="o">.</span><span class="n">any</span><span class="p">()</span> <span class="p">)</span> 

<span class="n">ratings_drama</span> <span class="o">=</span> <span class="n">ratings</span><span class="p">[</span> <span class="n">criterion</span> <span class="p">]</span>

<span class="c1">#  Plot ratings for drama movies </span>
<span class="n">rating_counts</span> <span class="o">=</span> <span class="n">ratings_drama</span><span class="p">[</span><span class="s1">&#39;rating&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">value_counts</span><span class="p">()</span>
<span class="n">sorted_counts</span> <span class="o">=</span> <span class="n">rating_counts</span><span class="o">.</span><span class="n">sort_index</span><span class="p">()</span>
<span class="n">sorted_counts</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span> <span class="n">kind</span> <span class="o">=</span> <span class="s1">&#39;bar&#39;</span><span class="p">,</span> <span class="n">color</span> <span class="o">=</span> <span class="s2">&quot;SteelBlue&quot;</span> <span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span> <span class="s1">&#39;Movie ratings for drama movies&#39;</span> <span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span> <span class="s1">&#39;Rating&#39;</span> <span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span> <span class="s1">&#39;Count&#39;</span> <span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt output_prompt">Out[5]:</div>



<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.text.Text at 0x11aca0908&gt;</pre>
</div>

</div>

<div class="output_area">
<div class="prompt"></div>



<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAh4AAAF+CAYAAADN3xONAAAABHNCSVQICAgIfAhkiAAAAAlwSFlz
AAAPYQAAD2EBqD+naQAAIABJREFUeJzs3X1YVHX+P/4nDAODIgM6AqYiH0QQEG/SNBXSBVzNe1hR
FDXLTJQCb7d1kzRcS828y/vW0BXTVlF2JW9abhI0V9MwbzBIQqlVkxG5U2aAmfP7oy/n5zggN+Jh
xOfjurgu531e5z2vc6B4cs6bg5kgCAKIiIiIJGDe1A0QERHR84PBg4iIiCTD4EFERESSYfAgIiIi
yTB4EBERkWQYPIiIiEgyDB5EREQkGQYPIiIikgyDBxEREUmGwYPIRJiZmSEhIaGp2xDt3LkTdnZ2
Td0GEhIS4ObmBplMhjlz5jz19xs8eLAk79Mc8FxRQzB4EFVj2rRpMDMzQ3h4uNG2iIgImJmZYdq0
aY36nrdu3cKrr77aqHPWlYuLC9atW2cwNmHCBGRnZzdJPw+bOXMmxo0bh19++QXLli1r6nboIQcP
HuTnhOqNwYOoBh07dsS+fftQVlYmjmk0GnzxxRdwdnZu9PdzcnKClZVVo80nCAIqKysbvL+1tTUc
HBwarZ+GKC0txZ07dzB06FC88MILaNWqVYPmKS8vb7SeGnOuZ13r1q0b/Dmh5xeDB1ENXnzxRXTs
2BEHDx4Uxw4ePAhnZ2f06tXLoFar1SIyMhIODg5QKBTw9fXFd999BwDQ6/Xo0KEDtmzZYrBPRkYG
zM3NcePGDQDGt1p++eUXjB8/HnZ2dmjdujXGjBmD69ev19jvN998AzMzMxw9ehS9e/eGlZUVTp48
iZycHIwZMwaOjo6wsbHBSy+9hKSkJHG/wYMH48aNG5g7dy7MzMxgZmYGwPhWy9KlS9GzZ0/s3r0b
Li4uUCqVCA0NRUlJiVhTUlKCsLAwtGzZEu3bt8eGDRuMLsdv3rwZXbp0gUKhgKOjI8aNG1fj8VR9
U/P394eZmRm++eYbAEB8fDy8vb1hZWUFFxcXfPLJJwb7uri4YNmyZZg6dSpsbW3x1ltvVfse9+/f
x9SpU2FjY4N27doZzfO4ud599124u7ujRYsWcHV1RXR0NCoqKozO1+effw5nZ2fY2Nhg9uzZ0Ol0
WLVqFZycnODg4IDly5cbvN+aNWvg4+ODli1bomPHjpg9ezZKS0ur7b+KmZkZtm3bhpEjR6JFixbw
9PTE6dOnce3aNQwePBgtW7bEgAEDkJOTY7Dfli1b0LlzZ1haWsLDwwO7d+8Wt02aNAkTJkwwqK+o
qIBKpcI//vEPAMa3WrRaLRYsWID27dujZcuW6Nevn/g5A4AbN25g1KhRsLe3R8uWLeHt7Y0jR448
9tioGRKIyMhrr70mjBkzRlizZo0QEBAgjgcEBAhr164VxowZI7z22mvieGRkpPDCCy8IR44cEa5c
uSK89tprgr29vXD37l1BEARhwYIFgq+vr8F7zJ8/32AMgHDo0CFBEAShvLxc8PT0FN544w3h4sWL
QmZmpjBp0iTBw8ND0Gq11facmpoqABC6d+8ufP3118K1a9eEu3fvChcuXBC2bt0qXLp0ScjOzhYW
L14sKBQK4caNG4IgCMLdu3eFDh06CDExMcKtW7eEW7duCYIgCLGxsYJSqRTnX7JkiWBjYyMEBwcL
ly5dEtLS0gQnJyfhr3/9q1jz5ptvCp06dRKSkpKES5cuCUFBQYKtra0QFRUlCIIgfPfdd4JMJhO+
+OIL4fr168L3338vrF+/vtrj0Wq1QlZWlgBAiI+PF27duiVotVrh3Llzgrm5uRATEyNkZWUJsbGx
grW1tRAbGyvu26lTJ8HW1lZYvXq1cO3aNeHatWvVvsesWbMEZ2dnISkpSbh48aIwcuRIoVWrVmK/
j5tr2bJlwqlTp4Tc3Fzh3//+t+Do6CisXLnS6HyNGzdOuHLlivDvf/9bsLS0FIYOHSq88847wo8/
/ih8/vnnAgDhv//9r7jf2rVrhZSUFCE3N1dITk4WPDw8hFmzZlXbfxUAQvv27YUvv/xSyMrKEsaO
HSu4uLgI/v7+wrFjx4TMzEzh5ZdfFoYNGybuc/DgQUEulwubNm0SsrKyhE8++USQyWRCSkqKIAiC
kJiYKFhbWwslJSXiPocPHxasra2F4uJiQRAEYdCgQQbn6s033xQGDBggpKWlCdeuXRM+/vhjwcrK
SsjOzhYEQRBGjBghDBkyRLh48aKQk5MjHD58WDhx4sRjj42aHwYPompUBY87d+4IVlZWwvXr14Xr
168LCoVCyM/PNwgepaWlglwuF/bs2SPuX15eLrzwwgvCqlWrBEEQhIyMDMHMzEz8Zq/T6YT27dsL
W7ZsEfd5OHjs3r1b8PDwEPR6vbhdq9UK1tbWwvHjx6vtuSp4JCQk1Hp83t7ewqeffiq+7tSpk7B2
7VqDmuqCR4sWLcRvOoIgCAsXLhT69esnCIIgFBcXC3K5XNi/f7+4vbCwUGjRooX4zSk+Pl6wtbU1
mONx7t27JwAQUlNTxbFJkyYJQ4YMMahbuHCh4OXlZXA8Y8eOfezcJSUlgqWlpfDPf/5THLt7965g
bW1tFDxqm0sQBOHjjz8WevfuLb6u7nwNHTpUcHFxEXQ6nTjm4eEhfPTRRzXOu3//fqFNmzaPfW8A
wuLFi8XXp0+fFgAIO3bsEMf27t0rKBQK8fWAAQOEGTNmGMwTEhIiDB8+XBAEQaioqBBUKpXwj3/8
Q9w+ceJEYcKECeLrh4PHjRs3BJlMJvzvf/8zmDMgIEBYtGiRIAiC4OPjIyxduvSxx0LNH2+1ED1G
27ZtMWLECOzcuROxsbEYMWIEVCqVQU1OTg4qKiowcOBAcUwul6Nv3764evUqAKBnz57w9PTEF198
AQA4ceIE7ty5g5CQkGrf94cffsC1a9fQqlUr2NjYwMbGBq1bt4ZGozG6XP6oPn36GLwuLS3FggUL
4OnpCTs7O9jY2ODq1avIy8ur9/lwcXExuKffrl073LlzBwDw888/o6KiAn379hW3K5VKeHh4iK+H
DBmCTp06wdXVFVOmTMGePXvw4MGDevVw9epVg3MNAAMHDsRPP/0EnU4njj16Hh6Vk5OD8vJy9OvX
Txxr3bq1Qb+Pm+vLL7/EwIED4eTkBBsbGyxevNjonD56vhwdHeHl5QVzc3ODsapzCABJSUkICAhA
+/bt0apVK0yZMgV3796t9Tx1797dYE4A8PHxMRjTaDQoLi4GUPN5rPqatbCwwPjx47Fnzx4Av9+W
+te//oWwsLBq3//SpUvQ6XRwd3cXv2ZtbGxw4sQJ8Ws2MjISf/vb3zBw4EAsWbIEFy9efOwxUfPE
4EFUizfeeAM7d+7Erl278MYbbzR4nrCwMDF4fPHFFxg2bBjatGlTbW1paSl69+6NCxcuGHxkZ2dj
0qRJj32fli1bGrxesGABDh06hA8//BDp6em4cOECfHx8GrRIUi6XG7w2MzODXq+v8/6tWrXC999/
j71796Jdu3Z4//330aNHDxQWFta7l9o8eh4ac67Tp08jLCwMw4cPR2JiIjIyMvDee+8ZndPqztfj
zuH169cxcuRIdO/eHfHx8Th//jw2bdoEoPZFrQ/PW7VOp7qx+ny+wsLCkJycjDt37iAhIQHW1tYY
NmxYtbWlpaWQyWQ4f/68wdfs1atXsX79egDAm2++iZ9//hlTpkzBpUuX0KdPH3z66ad17oeaBwYP
oloMGzYM5eXlqKiowNChQ422Vy3OO3XqlDhWUVGB7777Dl5eXuLYpEmTcPnyZZw/fx4HDhyo8SdH
4PeFrT/99BMcHBzg5uZm8KFUKuvV/6lTpzBt2jQEBQXBx8cHTk5ORotULS0tDa4WNISrqyvkcrm4
qBYAioqKjH4l18LCAoGBgVi1ahUuXryI69evIyUlpc7v4+npaXCugd+P0d3dHTKZrM7zdO7cGXK5
HGfOnBHH7t27V6dfIf7222/RqVMnvPfee+jTpw+6dOkiLhJ+EufPn4der8cnn3yCl19+Ge7u7rh5
8+YTz1udms7jw1+zAwYMQMeOHfHll19iz549CAkJMQpOVXr16gWdToc7d+4Yfc06OTmJdR07dkR4
eDgOHjyI+fPn47PPPnsqx0emy6KpGyAydTKZTLz8XN03tpYtW2LWrFlYuHAhWrduDWdnZ6xatQoP
HjzA9OnTxToXFxcMGDAA06dPh06nw+jRo2t8z7CwMHz88ccYM2YMYmJi0KFDB9y4cQMHDx7En//8
Z3To0KHO/Xfp0gUHDx7EqFGjYGZmhujoaKOfel1cXJCWlobQ0FBYWVkZ3U6qi1atWuG1114Tz4OD
gwOWLFkCc3Nz8aftxMRE/Pzzz3jllVdgb2+PI0eOQK/XV3t7oybz58/HSy+9hGXLlmHChAk4ffo0
Nm7ciM2bN9erXxsbG0yfPh0LFy5EmzZt4ODggPfee8/gNkhNunTpgry8POzbtw8vvfQSvvrqKxw6
dKhe718dNzc3VFRU4NNPP8WoUaNw6tQpbN269Ynnrc7ChQsxfvx49OrVC4GBgTh8+DAOHjxo8BtP
wO+BeevWrcjOzkZqamqN87m7uyMsLAxTp07FJ598gl69eiE/Px/Jycno3r07RowYgTlz5uDVV1+F
u7s77t27h9TUVHh6ej6V4yPTxSseRHVga2sLW1vbGrevWLECf/rTnzBlyhS8+OKLuHbtGo4fPw57
e3uDurCwMPzwww8ICgqCtbV1jfO1aNECaWlpcHZ2RnBwMDw9PTF9+nRoNJrH9lGdNWvWwN7eHgMG
DMCoUaMwdOhQvPjiiwY1MTExuH79Ojp37oy2bdvWa/5H36t///4YOXIkAgMDMXDgQHh6ekKhUAAA
7OzscPDgQfj7+8PT0xNbt27F3r174e3tXef3ePHFF/HPf/4T+/btQ7du3fD+++8jJiamQQ90+/jj
j+Hn54dRo0YhMDAQvr6+6N27d637jR49GnPnzsXbb7+Nnj174ttvv0V0dHS93/9RPXr0wJo1a7By
5Up069YNe/bswUcfffTE81Zn7NixWL9+PVavXg1vb29s27YNsbGxGDx4sEFdWFgYMjMz0b59e6M1
IY+KjY3F1KlTMX/+fHh4eGDs2LH47rvvxOfe6HQ6REREwNPTE8OGDYO7u3u9AyM9+8wEQRCaugki
ap7u37+P9u3b45NPPjG4+kNEzy/eaiGiRpORkYEff/wRffv2RVFREWJiYgAAY8aMaeLOiMhUMHgQ
UaNavXo1srKyYGlpid69eyM9Pb1Ba0aIqHnirRYiIiKSDBeXEhERkWQYPIiIiEgyDB5EREQkGS4u
lcjkyZNRUVEBc3Pzej95koiIyBQUFRVBr9dDLpcjLi6uQXMweEikoqICgiBAp9OhoKCgqdshIiJq
sIqKigbvy+AhEXNzc+h0OpiZmRk9zZKIiOhZcO/ePQiCUKc/LVATBg+JKJVKFBQUwN7e/qn97QUi
IqKnKTw8HAUFBU+0ZICLS4mIiEgyDB5EREQkGQYPIiIikgyDBxEREUmGwYOIiIgkw+BBREREkmHw
ICIiIskweBAREZFkGDyIiIhIMgweREREJBkGDyIiIpIM/1YLERE1maHLvmrU+Y5Hj2jU+ajx8YoH
ERERScakrnjk5ORg+/bt+PHHH6FWq6FQKODq6oopU6bglVdeMajNzc3FmjVrcOHCBcjlcgwcOBDz
5s2r9k/OJyQkIC4uDjdv3oSjoyMmTJiA0NBQo7qSkhJs2LABqamp0Gg08Pb2xty5c9G1a9endsxE
RETPE5O64nHr1i08ePAAI0aMwIIFC/Dmm28CAObNm4eDBw+Kdb/99htmzJiBX375BREREZg8eTJO
nTqFiIgIVFRUGMwZHx+Pv/3tb3B1dcXChQvh4+OD1atXY+fOnQZ1er0eUVFROHbsGMaPH4/IyEjc
u3cPM2fORF5e3lM/diIioueBSV3x8PX1ha+vr8HY+PHjMWXKFOzZswfBwcEAgNjYWJSVlSEuLg5O
Tk4AAG9vb0RERODw4cNinUajwebNm+Hr64tVq1YBAIKCgiAIAnbs2IHg4GDY2toCAJKTk3Hx4kWs
WLECgYGBAIAhQ4YgODgY27Ztw/LlyyU5B0RERM2ZSV3xqI5MJoOjoyNKS0vFsZSUFPj5+YmhAwD6
9esHZ2dnJCUliWPnzp1DUVERxo0bZzBnSEgIysrKcPLkSXEsOTkZbdq0gb+/vzhmb2+PwMBAnDhx
AuXl5U/j8IiIiJ4rJhk8ysrKUFhYiF9//RV79uzBt99+i5deegkAcOfOHRQUFMDT09NoP29vb2Rl
ZYmvq/7t5eVlUOfp6Qlzc3OjWg8PD5ibG54Sb29vaDSax95uKSsrq/VDp9PV/0QQERE1MyZ1q6XK
2rVrxTUd5ubm+MMf/oA///nPAAC1Wg0AUKlURvupVCoUFRWhvLwclpaWUKvVkMlkaN26tUGdXC6H
UqlEfn6+OKZWq9GrV69q5wSA/Px8uLm5Vduvn59fnY7L1dW1TnVERETNlUkGj0mTJiEgIAD5+flI
SkqCXq8XF41qtVoAgKWlpdF+VlZWYo2lpSW0Wi0sLKo/xKrtVar2edycRERE9GRMMni4uLjAxcUF
ADBy5EhERERg7ty52LVrlxgEqltzURUOqmqsrKxQWVlZ7XuUl5eLdVW1dZmzOunp6bUeU2RkJIqK
imqtIyIias5Mco3HowICApCZmYkbN26Itz6qbrk8TK1WQ6lUilcuVCoVdDodCgoKDOoqKipQVFSE
tm3bimMqlarGOQEY1D7K2tq61g+ZTFb/AyciImpmnongUXXVobS0FA4ODrC3t8fVq1eN6q5cuQJ3
d3fxtYeHBwAgMzPToC4zMxN6vd6g1t3dHVlZWdDr9UZzKhQKODs7N9rxEBERPa9MKng8emUCACor
K/HVV1/ByspKXJzp7++P9PR03L59W6w7e/Ys8vLyEBAQII716dMHSqUS8fHxBnMeOHAACoXC4Jkh
AQEBuHv3LlJSUsSxwsJCJCUlwc/Pr9r1H0RERFQ/JrXG48MPP8T9+/fRq1cvODg4QK1W49ixY7h+
/TrmzJmDFi1aAABef/11JCUlITw8HKGhoSgrK8Pu3bvh5uaG0aNHi/MpFAqEh4dj5cqVePfdd9G/
f39kZGTg6NGjmD17NpRKpVgbEBAAHx8fxMTEIDc3F3Z2dti/fz/0ej1mzpwp+bkgIiJqjkwqeAwZ
MgT/+te/EB8fj8LCQrRs2RJdu3bFO++8g0GDBol1Tk5O2L59O9auXYuNGzdCLpfD19cXc+bMMboy
ERISAgsLC8TFxSEtLQ2Ojo6YN28eJk6caFAnk8mwfv16rF+/Hvv27YNWq4WXlxeWLl0qLnQlIiKi
J2MmCILQ1E08D8LDw1FQUIDWrVtj69atTd0OEZFJGLrsq0ad73j0iEadjww1xvcyk1rjQURERM0b
gwcRERFJhsGDiIiIJMPgQURERJJh8CAiIiLJMHgQERGRZBg8iIiISDIMHkRERCQZBg8iIiKSDIMH
ERERSYbBg4iIiCTD4EFERESSYfAgIiIiyTB4EBERkWQYPIiIiEgyDB5EREQkGQYPIiIikgyDBxER
EUmGwYOIiIgkw+BBREREkmHwICIiIskweBAREZFkGDyIiIhIMgweREREJBkGDyIiIpIMgwcRERFJ
hsGDiIiIJMPgQURERJJh8CAiIiLJMHgQERGRZCyauoGHXblyBYmJiTh//jxu3rwJpVIJHx8fzJo1
C506dRLrli5disTERKP9O3XqhPj4eKPxhIQExMXF4ebNm3B0dMSECRMQGhpqVFdSUoINGzYgNTUV
Go0G3t7emDt3Lrp27dq4B0pERPScMqngsWvXLvzwww8IDAxEly5doFarsX//fkyePBmxsbFwc3MT
ay0tLbF48WKD/W1sbIzmjI+Px0cffQR/f3+EhYUhIyMDq1evhkajwbRp08Q6vV6PqKgo/PTTT5gy
ZQrs7Oxw4MABzJw5E7t374azs/NTO24iIqLnhUkFj7CwMCxfvhxyuVwc++Mf/4jQ0FDs2rULy5Yt
E8dlMhmGDx/+2Pk0Gg02b94MX19frFq1CgAQFBQEQRCwY8cOBAcHw9bWFgCQnJyMixcvYsWKFQgM
DAQADBkyBMHBwdi2bRuWL1/e2IdLRET03DGpNR49evQwCB0A4OzsDFdXV+Tm5hrV63Q6lJaW1jjf
uXPnUFRUhHHjxhmMh4SEoKysDCdPnhTHkpOT0aZNG/j7+4tj9vb2CAwMxIkTJ1BeXt7QwyIiIqL/
x6SCR3UEQUBBQQHs7OwMxjUaDQYNGoTBgwfD398fK1euxIMHDwxqsrKyAABeXl4G456enjA3Nxe3
V9V6eHjA3NzwlHh7e0Oj0SAvL6/GHsvKymr90Ol0DTp+IiKi5sSkbrVU5+jRo7hz5w5mzpwpjqlU
KkydOhVdu3aFXq/H6dOnsX//fmRnZ2Pbtm2wsPj9sNRqNWQyGVq3bm0wp1wuh1KpRH5+vjimVqvR
q1cvo/dXqVQAgPz8fIM1Jg/z8/Or07G4urrWqY6IiKi5Mungcf36daxcuRLdu3fHyJEjxfG3337b
oG7o0KFwdnbG5s2bkZycjKFDhwIAtFqtGEIeZWlpCa1WK77WarWwtLQ0qrOyshK3ExER0ZMx2eCh
VqsRFRUFGxsbrFy5EjKZ7LH1kyZNwtatW3H27FkxeFhZWaGysrLa+vLycjFUVNVWt46jKnA8XPuo
9PT0Wo8nMjISRUVFtdYRERHVxdBlXzXqfMejRzTqfDUxyeBRWlqKyMhIlJaW4rPPPkPbtm1r3Ueh
UECpVKK4uFgcU6lU0Ol0KCgoMLjdUlFRgaKiIoN5VSoV1Gq10bxVY4/rwdrautb+agtOREREzwOT
W1yq1Woxd+5c5OXlYe3atXVeF3H//n0UFhYaLEL18PAAAGRmZhrUZmZmQq/Xw93dXRxzd3dHVlYW
9Hq9Qe2VK1egUCj4HA8iIqJGYFLBQ6fTYdGiReLzNLp3725Uo9Vqcf/+faPxv//97xAEAQMGDBDH
+vTpA6VSafQ00wMHDkChUMDX11ccCwgIwN27d5GSkiKOFRYWIikpCX5+ftWu/yAiIqL6MalbLevW
rUNaWhr8/PxQXFyMI0eOGGwfPnw47t69i7CwMAwdOhQuLi4AgNOnT+PUqVMYMGAABg0aJNYrFAqE
h4dj5cqVePfdd9G/f39kZGTg6NGjmD17NpRKpVgbEBAAHx8fxMTEIDc3F3Z2dti/fz/0er3Bb9QQ
ERFRw5lU8Kh6rkZ6enq1CzaHDx+OVq1awdfXF2fOnEFiYiL0ej06dOiAiIgITJkyxeg5HCEhIbCw
sEBcXBzS0tLg6OiIefPmYeLEiQZ1MpkM69evx/r167Fv3z5otVp4eXlh6dKlYsAhIqLnx7O6eNPU
mVTw2L59e601rVq1Mnh0el0EBQUhKCio1jpbW1tER0cjOjq6XvMTERFR3ZjUGg8iIiJq3hg8iIiI
SDIMHkRERCQZBg8iIiKSDIMHERERSYbBg4iIiCTD4EFERESSYfAgIiIiyTB4EBERkWQYPIiIiEgy
DB5EREQkGQYPIiIikgyDBxEREUmGwYOIiIgkY9HUDRAR0dMzdNlXjTrf8egRjTofPX94xYOIiIgk
w+BBREREkmHwICIiIskweBAREZFkGDyIiIhIMgweREREJBkGDyIiIpIMgwcRERFJhsGDiIiIJMPg
QURERJJh8CAiIiLJMHgQERGRZBg8iIiISDIMHkRERCQZi6Zu4GFXrlxBYmIizp8/j5s3b0KpVMLH
xwezZs1Cp06dDGpzc3OxZs0aXLhwAXK5HAMHDsS8efNgb29vNG9CQgLi4uJw8+ZNODo6YsKECQgN
DTWqKykpwYYNG5CamgqNRgNvb2/MnTsXXbt2fWrHTERE9DwxqeCxa9cu/PDDDwgMDESXLl2gVqux
f/9+TJ48GbGxsXBzcwMA/Pbbb5gxYwZsbGwQERGBBw8eIC4uDjk5Odi1axfkcrk4Z3x8PD766CP4
+/sjLCwMGRkZWL16NTQaDaZNmybW6fV6REVF4aeffsKUKVNgZ2eHAwcOYObMmdi9ezecnZ2lPh1E
RETNjkkFj7CwMCxfvtwgOPzxj39EaGgodu3ahWXLlgEAYmNjUVZWhri4ODg5OQEAvL29ERERgcOH
DyM4OBgAoNFosHnzZvj6+mLVqlUAgKCgIAiCgB07diA4OBi2trYAgOTkZFy8eBErVqxAYGAgAGDI
kCEIDg7Gtm3bsHz5csnOAxERUXNlUms8evToYRA6AMDZ2Rmurq7Izc0Vx1JSUuDn5yeGDgDo168f
nJ2dkZSUJI6dO3cORUVFGDdunMGcISEhKCsrw8mTJ8Wx5ORktGnTBv7+/uKYvb09AgMDceLECZSX
lzfacRIRET2vTCp4VEcQBBQUFMDOzg4AcOfOHRQUFMDT09Oo1tvbG1lZWeLrqn97eXkZ1Hl6esLc
3Nyo1sPDA+bmhqfE29sbGo0GeXl5NfZYVlZW64dOp6v/wRMRETUzJnWrpTpHjx7FnTt3MHPmTACA
Wq0GAKhUKqNalUqFoqIilJeXw9LSEmq1GjKZDK1btzaok8vlUCqVyM/PF8fUajV69epV7ZwAkJ+f
L64xeZSfn1+djsXV1bVOdURERM2VSV/xuH79OlauXInu3btj5MiRAACtVgsAsLS0NKq3srIyqNFq
tbCwqD5bWVpainVVtXWZk4iIiBrOZK94qNVqREVFwcbGBitXroRMJgPw/weB6tZcVIWDqhorKytU
VlZWO395eblYV1Vblzmrk56eXuvxREZGoqioqNY6IiKi5swkg0dpaSkiIyNRWlqKzz77DG3bthW3
Vd36qLrl8jC1Wg2lUileuVCpVNDpdCgoKDC43VJRUYGioiKjeWuaE4BB7aOsra1rPaaq4ERERPQ8
M7lbLVqtFnPnzkVeXh7Wrl1rtC7CwcEB9vb2uHr1qtG+V65cgbu7u/jaw8MDAJCZmWlQl5mZCb1e
b1Dr7u4hPnf+AAAgAElEQVSOrKws6PV6ozkVCgWf40FERNQITCp46HQ6LFq0SHyeRvfu3aut8/f3
R3p6Om7fvi2OnT17Fnl5eQgICBDH+vTpA6VSifj4eIP9Dxw4AIVCAV9fX3EsICAAd+/eRUpKijhW
WFiIpKQk+Pn5Vbv+g4iIiOrHpG61rFu3DmlpafDz80NxcTGOHDlisH348OEAgNdffx1JSUkIDw9H
aGgoysrKsHv3bri5uWH06NFivUKhQHh4OFauXIl3330X/fv3R0ZGBo4ePYrZs2dDqVSKtQEBAfDx
8UFMTAxyc3NhZ2eH/fv3Q6/Xi79RQ0RERE/GpIJH1XM10tPTq12wWRU8nJycsH37dqxduxYbN26E
XC6Hr68v5syZY3RlIiQkBBYWFoiLi0NaWhocHR0xb948TJw40aBOJpNh/fr1WL9+Pfbt2wetVgsv
Ly8sXboULi4uT+eAiYiInjMmFTy2b99e59rOnTtj48aNdaoNCgpCUFBQrXW2traIjo5GdHR0nfsg
IiKiujOpNR5ERETUvDF4EBERkWQYPIiIiEgyDQ4e4eHhOHv2bI3bz507h/Dw8IZOT0RERM1Qg4PH
+fPnUVBQUOP2goICfP/99w2dnoiIiJqhp3ar5ZdffkGLFi2e1vRERET0DKrXr9MmJiYiMTFRfP35
558jISHBqK6kpATXrl3DgAEDnrxDIiIiajbqFTw0Gg3u3bsnvr5//z7MzMwMaszMzGBtbY3g4GDM
mDGjcbokIiKiZqFewWPcuHEYN24cAGD06NGYP38+Bg0a9FQaIyIiouanwU8u/fe//92YfRAREdFz
4IkfmX7//n3cunULJSUlEATBaPuLL774pG9BREREzUSDg0dhYSFWrVqFlJQU6PV6o+2CIMDMzOyx
z/ogIiKi50uDg8fy5cuRlpaG0NBQ9OrVC61atWrMvoiIiKgZanDw+O9//4tJkyYhKiqqMfshIiKi
ZqzBDxBTKBR44YUXGrMXIiIiauYaHDxeffVVpKamNmYvRERE1Mw1+FZLQEAAvv/+e7zzzjsICgqC
o6MjZDKZUV3Xrl2fqEEiIiJqPhocPN58803x32fOnDHazt9qISIiokc1OHgsWbKkMfsgIiKi50CD
g8fIkSMbsw8iIiJ6DjR4cSkRERFRfTX4iscHH3xQa42ZmRnef//9hr4FERERNTMNDh7nzp2DmZmZ
wZhOp4NarYZer4e9vT2sra2fuEEiIiJqPhocPA4fPlzteGVlJeLj47F3715s2rSpwY0RERFR89Po
azwsLCwwYcIEvPzyy1i1alVjT09ERETPsKe2uLRLly7IyMh4WtMTERHRM+ipBY8zZ85AoVA8remJ
iIjoGdTgNR6fffZZteMlJSXIyMjAjz/+iGnTpjV0eiIiImqGGhw8tm/fXu24ra0t2rdvj0WLFiEo
KKjBjREREVHz0+Dg8d133zVmH0RERPQcaHDweBoePHiA3bt34/Lly7hy5QqKi4uxZMkSjBo1yqBu
6dKlSExMNNq/U6dOiI+PNxpPSEhAXFwcbt68CUdHR0yYMAGhoaFGdSUlJdiwYQNSU1Oh0Wjg7e2N
uXPn8i/sEhERNZInDh7nz5/HyZMncfv2bQCAk5MTfH190bt373rPVVhYiM8++wxOTk7o0qULzp8/
X2OtpaUlFi9ebDBmY2NjVBcfH4+PPvoI/v7+CAsLQ0ZGBlavXg2NRmOwBkWv1yMqKgo//fQTpkyZ
Ajs7Oxw4cAAzZ87E7t274ezsXO/jISIiIkMNDh4VFRX461//ihMnTkAQBLRq1QrA71cN9uzZg8GD
B+PDDz+EhUXd30KlUuHYsWNQqVTIzMzE1KlTa6yVyWQYPnz4Y+fTaDTYvHkzfH19xWeKBAUFQRAE
7NixA8HBwbC1tQUAJCcn4+LFi1ixYgUCAwMBAEOGDEFwcDC2bduG5cuX1/k4iIiIqHoN/nXa7du3
45tvvkFYWBiOHTuGlJQUpKSk4Pjx45g8eTJSU1Nr/M2XmlhaWkKlUtW5XqfTobS0tMbt586dQ1FR
EcaNG2cwHhISgrKyMpw8eVIcS05ORps2beDv7y+O2dvbIzAwECdOnEB5eXk9joSIiIiq0+Dgcfz4
cYwcORJRUVFo06aNON66dWtERkZixIgROHLkSKM0WR2NRoNBgwZh8ODB8Pf3x8qVK/HgwQODmqys
LACAl5eXwbinpyfMzc3F7VW1Hh4eMDc3PCXe3t7QaDTIy8ursZeysrJaP3Q63ZMeMhER0TOvwbda
1Go1vL29a9zerVs3fP311w2d/rFUKhWmTp2Krl27Qq/X4/Tp09i/fz+ys7Oxbds28faOWq2GTCZD
69atDfaXy+VQKpXIz883OJ5evXpV+14AkJ+fDzc3t2r78fPzq1Pfrq6udaojIiJqrhocPBwcHHD+
/Hmj2xhVzp8/DwcHhwY39jhvv/22weuhQ4fC2dkZmzdvRnJyMoYOHQoA0Gq1Na4xsbS0hFarFV9r
tVpYWloa1VlZWYnbiYiI6Mk0OHiMHDkS27ZtQ6tWrTBp0iR07NgRZmZmyMvLw969e5GcnIy33nqr
MXt9rEmTJmHr1q04e/asGDysrKxQWVlZbX15ebkYKqpqq1vHURU4Hq59VHp6eq39RUZGoqioqNY6
IiKi5qzBweP111/Hr7/+ikOHDiEhIQFmZmYAAEEQIAgCRo4ciTfeeKPRGq2NQqGAUqlEcXGxOKZS
qaDT6VBQUGBwu6WiogJFRUVo27atQa1arTaat2rs4dpHWVtb19qfTCar03EQERE1Zw0OHjKZDEuX
LkVYWBhOnTqFW7duAQDatWuHgQMHokuXLo3WZF3cv38fhYWFsLOzE8c8PDwAAJmZmfD19RXHMzMz
odfr4e7uLo65u7vjwoUL0Ov1BgtMr1y5AoVCwed4EBERNYJ6BQ+tVotPPvkErq6u4pM/u3TpYhQy
9u3bh/j4eMyfPx9yubzxuv1/PVRWVqJly5YG43//+98hCAIGDBggjvXp0wdKpRLx8fEGwePAgQNQ
KBQGYwEBAUhOTkZKSor4HI/CwkIkJSXBz8+v2vUfREREVD/1Ch6HDh1CYmIi/vnPfz62ztfXFxs2
bMD//d//YcKECfVq6Msvv0RJSYl4iyMtLQ2//fYbACA0NBTFxcUICwvD0KFD4eLiAgA4ffo0Tp06
hQEDBmDQoEHiXAqFAuHh4Vi5ciXeffdd9O/fHxkZGTh69Chmz54NpVIp1gYEBMDHxwcxMTHIzc2F
nZ0d9u/fD71ej5kzZ9brGIiIiKh69Qoe//nPf+Dv748OHTo8tq5Dhw4ICAjA8ePH6x084uLixNs2
AJCamorU1FQAwPDhw9GqVSv4+vrizJkzSExMhF6vR4cOHRAREYEpU6YYPYcjJCQEFhYWiIuLQ1pa
GhwdHTFv3jxMnDjRoE4mk2H9+vVYv3499u3bB61WCy8vLyxdulQMOERERPRk6hU8rl27hldffbVO
tT169EBaWlq9Gzp8+HCtNcuWLavXnEFBQQgKCqq1ztbWFtHR0YiOjq7X/ERERFQ39XpyaWVlZZ3/
9oqFhUWNv8pKREREz6d6BQ+VSoWcnJw61ebk5NTr764QERFR81ev4NG3b18cOXIEBQUFj60rKCjA
kSNH0K9fvydqjoiIiJqXegWP1157DVqtFuHh4bh8+XK1NZcvX8asWbOg1Wof+2ftiYiI6PlTr8Wl
HTp0wIoVK/Dee+/hjTfeQPv27eHm5oYWLVrgwYMHyMnJwa+//gqFQoEPP/yw1t9+ISIioudLvZ9c
6uvri71792LXrl04efIkvvnmG3Fb27ZtMXbsWEydOpWhg4iIiIw06JHpL7zwAhYtWgTg90eV379/
Hy1btjR6migRERHRwxr8t1qqMHAQERFRXdVrcSkRERHRk2DwICIiIskweBAREZFkGDyIiIhIMgwe
REREJBkGDyIiIpIMgwcRERFJhsGDiIiIJMPgQURERJJh8CAiIiLJMHgQERGRZBg8iIiISDIMHkRE
RCQZBg8iIiKSDIMHERERSYbBg4iIiCTD4EFERESSYfAgIiIiyTB4EBERkWQYPIiIiEgyDB5EREQk
GQYPIiIikoxFUzfwsAcPHmD37t24fPkyrly5guLiYixZsgSjRo0yqs3NzcWaNWtw4cIFyOVyDBw4
EPPmzYO9vb1RbUJCAuLi4nDz5k04OjpiwoQJCA0NNaorKSnBhg0bkJqaCo1GA29vb8ydOxddu3Z9
KsdLRET0vDGpKx6FhYX47LPPkJubiy5dutRY99tvv2HGjBn45ZdfEBERgcmTJ+PUqVOIiIhARUWF
QW18fDz+9re/wdXVFQsXLoSPjw9Wr16NnTt3GtTp9XpERUXh2LFjGD9+PCIjI3Hv3j3MnDkTeXl5
T+NwiYiInjsmdcVDpVLh2LFjUKlUyMzMxNSpU6uti42NRVlZGeLi4uDk5AQA8Pb2RkREBA4fPozg
4GAAgEajwebNm+Hr64tVq1YBAIKCgiAIAnbs2IHg4GDY2toCAJKTk3Hx4kWsWLECgYGBAIAhQ4Yg
ODgY27Ztw/Lly5/24RMRETV7JnXFw9LSEiqVqta6lJQU+Pn5iaEDAPr16wdnZ2ckJSWJY+fOnUNR
URHGjRtnsH9ISAjKyspw8uRJcSw5ORlt2rSBv7+/OGZvb4/AwECcOHEC5eXlNfZTVlZW64dOp6vT
OSAiImrOTOqKR13cuXMHBQUF8PT0NNrm7e2Nb7/9VnydlZUFAPDy8jKo8/T0hLm5ObKysjB8+HCx
1sPDA+bmhlnM29sbhw4dQl5eHtzc3Krtyc/Pr069u7q61qmOiJ4tQ5d91ajzHY8e0ajzEZkSk7ri
URdqtRoAqr0yolKpUFRUJF6dUKvVkMlkaN26tUGdXC6HUqlEfn6+wbw1zQnAoJaIiIga5pm74qHV
agH8flvmUVZWVmKNpaUltFotLCyqP8Sq7Q/PW9ucNUlPT6+178jISBQVFdVaR0RE1Jw9c8GjKghU
t+aiKhxU1VhZWaGysrLaecrLy8W6qtq6zFkda2vrWvuWyWS11hARETV3z9ytlqpbH1W3XB6mVquh
VCrFKxcqlQo6nQ4FBQUGdRUVFSgqKkLbtm0N5q1pTgAGtURERNQwz1zwcHBwgL29Pa5evWq07cqV
K3B3dxdfe3h4AAAyMzMN6jIzM6HX6w1q3d3dkZWVBb1ebzSnQqGAs7NzYx4GERHRc+mZCx4A4O/v
j/T0dNy+fVscO3v2LPLy8hAQECCO9enTB0qlEvHx8Qb7HzhwAAqFAr6+vuJYQEAA7t69i5SUFHGs
sLAQSUlJ8PPzq3b9BxEREdWPya3x+PLLL1FSUiLe4khLS8Nvv/0GAAgNDYWNjQ1ef/11JCUlITw8
HKGhoSgrK8Pu3bvh5uaG0aNHi3MpFAqEh4dj5cqVePfdd9G/f39kZGTg6NGjmD17NpRKpVgbEBAA
Hx8fxMTEIDc3F3Z2dti/fz/0ej1mzpwp7UkgIiJqpkwueMTFxeHWrVvi69TUVKSmpgIAhg8fDhsb
Gzg5OWH79u1Yu3YtNm7cCLlcDl9fX8yZM8foykRISAgsLCwQFxeHtLQ0ODo6Yt68eZg4caJBnUwm
w/r167F+/Xrs27cPWq0WXl5eWLp0KVxcXJ76cRMRET0PTC54HD58uE51nTt3xsaNG+tUGxQUhKCg
oFrrbG1tER0djejo6DrNS0RERPXzTK7xICIiomcTgwcRERFJhsGDiIiIJMPgQURERJJh8CAiIiLJ
MHgQERGRZBg8iIiISDIMHkRERCQZBg8iIiKSDIMHERERSYbBg4iIiCTD4EFERESSYfAgIiIiyTB4
EBERkWQYPIiIiEgyDB5EREQkGQYPIiIikgyDBxEREUmGwYOIiIgkw+BBREREkmHwICIiIskweBAR
EZFkGDyIiIhIMgweREREJBkGDyIiIpIMgwcRERFJhsGDiIiIJMPgQURERJJh8CAiIiLJWDR1Aw1x
7tw5hIeHV7stNjYWPj4+4uvc3FysWbMGFy5cgFwux8CBAzFv3jzY29sb7ZuQkIC4uDjcvHkTjo6O
mDBhAkJDQ5/acRARET1vnsngUSU0NBReXl4GYx07dhT//dtvv2HGjBmwsbFBREQEHjx4gLi4OOTk
5GDXrl2Qy+VibXx8PD766CP4+/sjLCwMGRkZWL16NTQaDaZNmybVIRERETVrz3Tw6NmzJwIDA2vc
Hhsbi7KyMsTFxcHJyQkA4O3tjYiICBw+fBjBwcEAAI1Gg82bN8PX1xerVq0CAAQFBUEQBOzYsQPB
wcGwtbV9+gdERETUzD3zazzu37+PysrKarelpKTAz89PDB0A0K9fPzg7OyMpKUkcO3fuHIqKijBu
3DiD/UNCQlBWVoaTJ08+neaJiIieM8/0FY+YmBg8ePAAMpkMPXv2RFRUlHjr5c6dOygoKICnp6fR
ft7e3vj222/F11lZWQBgdNvG09MT5ubmyMrKwvDhw2vso6ysrNZedTpdnY6JiIioOXsmg4dcLoe/
vz8GDhwIOzs75ObmYvfu3ZgxYwZ27NiBrl27Qq1WAwBUKpXR/iqVCkVFRSgvL4elpSXUajVkMhla
t25t9D5KpRL5+fmP7cfPz69Ofbu6utbxCInoYUOXfdWo8x2PHtGo8xFR3T2TwaNHjx7o0aOH+HrQ
oEEICAhAaGgoNm3ahE8//RRarRYAYGlpabS/lZUVAECr1cLS0hJarRYWFtWfiqrtRERE9OSeyeBR
nY4dO2LQoEFITU2FTqcTw0V5eblRbVWQqKqxsrKqcZ1IeXm5WFeT9PT0WvuLjIxEUVFRrXVERETN
WbMJHgDg6OiIiooKlJWVibdYqm65PEytVkOpVIpXQ1QqFXQ6HQoKCgxut1RUVKCoqAht27Z97Pta
W1vX2ptMJqvPoRARETVLz/xvtTzsf//7H6ysrNCiRQs4ODjA3t4eV69eNaq7cuUK3N3dxdceHh4A
gMzMTIO6zMxM6PV6g1oiIiJquGcyeNy7d89oLDs7G2lpaejXrx/MzX8/LH9/f6Snp+P27dti3dmz
Z5GXl4eAgABxrE+fPlAqlYiPjzeY88CBA1AoFPD19X1KR0JERPR8eSZvtSxatAhWVlbo3r07Wrdu
jZ9//hmHDh2CQqHAO++8I9a9/vrrSEpKQnh4OEJDQ1FWVobdu3fDzc0No0ePFusUCgXCw8OxcuVK
vPvuu+jfvz8yMjJw9OhRzJ49G0qlsikOk4iIqNl5JoPH4MGDcfToUXzxxRcoLS2Fvb09/vCHP+Ct
t94yeGS6k5MTtm/fjrVr12Ljxo2Qy+Xw9fXFnDlzjH7bJSQkBBYWFoiLi0NaWhocHR0xb948TJw4
UerDIyIiaraeyeARGhpa5z/e1rlzZ2zcuLFOtUFBQQgKCnqS1oiIiOgxnsk1HkRERPRsYvAgIiIi
yTB4EBERkWQYPIiIiEgyDB5EREQkGQYPIiIikgyDBxEREUmGwYOIiIgkw+BBREREkmHwICIiIskw
eBAREZFkGDyIiIhIMgweREREJBkGDyIiIpIMgwcRERFJhsGDiIiIJMPgQURERJKxaOoGiMg0DF32
VaPNdTx6RKPNRUTNC694EBERkWQYPIiIiEgyDB5EREQkGQYPIiIikgyDBxEREUmGwYOIiIgkw+BB
REREkmHwICIiIskweBAREZFk+ORSqpfGfLol8Hw94ZLnjoiIwYOaGT72m4jItPFWCxEREUmGVzwe
UV5ejq1bt+LIkSMoKSmBm5sbZs2ahZdffrmpWyMiInrm8YrHI5YuXYo9e/bg1Vdfxfz58yGTyRAV
FYULFy40dWtERETPPAaPh1y+fBlff/013n77bURFRSE4OBhbtmxBu3btsGHDhqZuj4iI6JnH4PGQ
5ORkyGQyBAUFiWNWVlYYM2YMLl68iNu3bzdhd0RERM8+rvF4SFZWFpydnWFjY2Mw7u3tDQDIzs6G
k5OT0X5lZWW1zq3T6RqnSSIiomeYmSAIQlM3YSrGjx+PNm3aYMuWLQbjP//8M8aPH49FixbhT3/6
k9F+ffr0qdP8rq6uMDMzg729/WPr1MWaujddC5WtotHmAhq3N8C0+zPl3gDT7s+UewOer/5MuTfA
tPsz5d6Apunv3r17EAQBMpkMe/fubdD78IrHQ7RaLeRyudG4paWluP1JCYKAgoKCx9Y87v6XXq/H
9evXAQAuLi4wN3/83bKCggf17PDxars315z6M+XeANPuz5R7A56v/ky5N8C0+zPl3oCm7U+v19e5
9lEMHg+xsrJCRUWF0Xh5ebm4vTrp6em1zj19+nTodDqYm5tDqVQ2uEedTid+Idnb20MmkzV4rqeB
/TWcKfcGmHZ/ptwbYNr9mXJvgGn3Z8q9AU+nv6KiIuj1+mp/SK8r3mp5yOzZs5Gfn4/9+/cbjJ89
exazZ8/GmjVr8MorrzRRd78rKyuDn58fgN8Dj7W1dZP28yj213Cm3Btg2v2Zcm+Aafdnyr0Bpt2f
KfcGmG5//K2Wh3h4eCAvLw+lpaUG45cvXwYAuLu7N0VbREREzQaDx0MCAgKg0+lw6NAhcay8vByH
Dx9Gt27dqv2NFiIiIqo7rvF4SLdu3RAYGIiNGzeioKAAHTt2RGJiIm7evIno6Oimbo+IiOiZx+Dx
iA8++ADt2rUz+Fst69atw4svvtjUrRERET3zGDweYWVlhaioKERFRTV1K0RERM0O13gQERGRZBg8
iIiISDJ8jgcRERFJhlc8iIiISDIMHkRERCQZBg8iIiKSDIMHERERSYbBg4iIiCTD4EFEdVZcXIw1
a9YgJyenqVshomcUn1z6jLhz5w6ys7ORn58PrVYLKysrtG3bFu7u7nBwcGjq9mp1//59lJSU8A/t
1UHVX0h2dXWFQqFo6nYM3L9/H/v27UOfPn3QuXPnpm7HgCAIKCsrQ4sWLZq6FSO//vorLl68iOLi
Ytjb26N3795QqVSS96FWq5vkfeujtLQUFhYWBl/7xcXFyMrKgk6ng5ubW5Meg0ajwbVr18T/F1tb
W6NTp05wcXFpsp6eNXyOh4n74YcfsGHDBly6dAnA7/9zfZiZmRm6deuGyMhI9OzZsylarJMdO3Zg
27ZtOHv2rGTv+fPPP2Pnzp24fv067Ozs8Mc//hEjRoyAmZmZQd3Ro0exZMkSSXtLSEjAnj17UFJS
gr59++LPf/4zysvLMW/ePGRmZgL4/fH9s2fPxsSJEyXrKzQ09LHbKysrcePGDbRr1w4tWrSAmZkZ
9u7dK1F3wOXLl9GxY0colUpxLDs7Gxs3bsT58+dRUVEBS0tL9O/fHxEREZJ/M/jyyy9x584dvPPO
OwB+/+vWMTEx+Prrrw3+27WwsMDUqVMxa9YsSfvr27cvXF1dMWzYMAwbNsykfhDQaDRYvHgx0tLS
YGZmhokTJ2LOnDnYv38/Pv30U2g0GgC//z9vzJgx+Mtf/gJzc+ku2ufl5WHTpk04efIkKioqjLY7
ODhg0qRJCA0NlbSvx6msrIRGo4FCoYCFhelcZzCdTsjImTNnEBUVhXbt2mH27Nnw9vaGSqWCpaUl
ysvLoVarcenSJSQmJmLWrFlYt24d+vXr19Rtm4S8vDxMmzYNOp0Orq6uyMnJwQcffICEhASsWLGi
SX9iSk9Px/Lly9GlSxd4enri+PHjqKiogE6ng42NDRYtWgStVovExESsXbsWHTt2hK+vryS95eTk
oEWLFujatWu128vLywEA1tbWBt/8pfLGG28gJiYGw4YNAwBcvXoVM2bMAAAMHjwYjo6O+PXXX5Ge
no7vv/8eu3btQocOHSTr7+DBg3jllVfE12vWrMHx48cRHByMYcOGwd7eHmq1GocOHUJsbCzs7e1r
DXuNSRAE/O9//8OmTZuwZcsW9OjRA8OGDUNgYCBsbW0l66M6cXFxOHHiBEaMGIE2bdogPj4eCoUC
n3/+OUaMGIFBgwahsrISx44dQ0JCAl544QVMmzZNkt6ys7Mxc+ZM6PV69O3bFwqFApcvX8bdu3cx
depU6HQ6nDlzBmvXrsXZs2exevXqJvlGX1lZicTERPznP/9BVlYWiouLxW22trZwd3fHkCFDMGrU
qCYNIrziYcKmTZsGmUyGLVu2wNLSssa6iooK8T+KnTt3StZfYmJinWvT0tLwzTffSHZVYdGiRfj+
++/x97//HR07dgQAHDlyBKtWrYKtrS02bNgg/jQs9RWPt956CwCwbds2mJmZYc+ePdiwYQMGDBiA
tWvXinWVlZWYOHEiHB0dsXHjRkl627FjB3bu3AkfHx/Mnz/f6HbKzZs3MWbMGKxevRqDBg2SpKeH
vfTSS1i2bJkYPMLDw5GTk4PY2FiDgJGdnY3p06cjICAAS5culaw/X19fLFiwAGPHjoUgCBg0aBDG
jBmD+fPnG9X+5S9/QXZ2Ng4ePChZfy+99BJiYmLQrl07HDt2DElJSSgqKoJcLkf//v3x6quvws/P
D1ZWVpL1VGXcuHHo3r073n//fQDA119/jcWLF2P06NFYvHixQW1kZCRu3ryJAwcOSNLb22+/jV9+
+QU7duwQf2iprKxEdHQ0bt68iV27dok9R0dHIyIiAlOnTpWktyqFhYWIiIhAdnY2nJ2dxR9Urays
oNVqoVarceXKFeTl5aFLly7YtGkT7O3tJe2xCq94mLCffvoJCxcufGzoAAC5XI5Ro0Zh9erVEnX2
uw8++ABmZmZGt39q8ugtjqfp0qVLmDBhghg6AGD48OHw8vJCVFQU3nzzTaxbtw7dunWTrKcqP//8
M958803xfAwaNAjr1q3DkCFDDOosLCwwbNgwfPHFF5L1Nn36dIwaNQpr165FWFgYgoKCEB4eLl7d
kPJzWBudToeMjAzMnj3b6KqGu7s7xo4di+TkZEl7srKyQllZGQBAq9WirKwMvXv3rra2T58+SEtL
kxrCBigAAAu3SURBVLI9AL9/Dnv27ImePXtiwYIFOH36NI4dO4a0tDSkp6fD2toa/v7+GDZsGPr2
7SvZ5/z27duYPHmy+LpHjx4Q/r/27j8m6jKOA/ib3+cJBAfkYEgUzYALiqTwR6c3QzQ2DAIk/LVh
ZHiULGghmw1YzdYsxDklzLnZboEhNAICZiQ5yQYRDs0Zi8a8JnYQHQnYeXL0B+ObcJeKP54Dfb/+
4vvc5+75gHJ87nk+3+93bMzqat+yZctQVFQkJC9g/P3ktddem7RS6ujoiFdffRXr1q1Dd3c3goKC
EBMTg9bWVtTW1govPIqKinDp0iXs27cPzz333P/Gtba2Ii8vD8XFxSgsLBSY4X9YeMxg7u7u0Ol0
txSr0+mEL5VOLN1t27btprHV1dVCP9kNDg7Cy8vLYjwwMBCHDh3Cm2++CY1Ggw8//FBYThMm9lwn
uLq6AgB8fHwsYr28vDAyMiIsN2B8r/qDDz7ATz/9hI8++ggJCQlIT0/H2rVrheZxM0ajEWazGY89
9pjVx4OCgoR9Ip4QHh6OY8eOITU1FTKZDAEBAWhvb4darbaIbW9vt/pvLpKjoyNUKhVUKhWuXLmC
48ePo6GhAfX19airq4NCoUBDQ4OQXB566CEMDg5KxxNfXz82wWAwCN/qs9a34eDggLGxMQwNDUlj
YWFhqK+vF5kaAKClpQUbN268YdEBjPf5bNiwAVqtVlBmllh4zGAvvvgiPv/8cygUCiQkJFjt1h8Z
GUFVVRXKysqENiECgFKpRE9PD0JCQm4a+/333wvI6D++vr749ddfrT7m5eWFAwcO4K233kJ2djaW
LFkiNDcvLy/09/dLxzKZDC+//LLVs5P6+vps0ksBAM888wy0Wi2OHj2K0tJSHD16FK+88orNVz3O
nTsnrQLK5XIYDAarcQMDA5g7d67I1PD6669j8+bNyM3NhUajQW5uLnJycnDt2jWsWrUKCoUCer0e
1dXVaGpqkrbdZoI5c+YgNjYWsbGxMBgMaGxsRGNjo7D5w8PDUVVVheXLl8PT0xOlpaVwcXFBU1MT
li5dKq026HQ6VFRU3NL7zt3MrbKyEnFxcXBzcwMw3i/z2WefwcnJadKW5ODgoPD/d8D4lvutntEl
l8utNsiKwsJjBtu6dSsuXbqE4uJi7N27FwEBARbNpRcuXMDo6Ciio6OFd8grlUqcOnUKAwMDUCgU
N4x1c3MT2kG/cOFCfPPNN8jKyrLaROXq6op9+/Zh+/btUhe9KCEhIejs7JSOZTIZ8vLyrMZ2dHTg
8ccfF5WaBXt7e6xduxarVq3C/v378fHHH9sslwllZWWTzqRpaWlBXFycRVxnZ+ekrTYRgoODUVRU
hPz8fCQnJ0t/gCorK1FZWSnFjY2NYc2aNUhLSxOa363y8PBASkoKUlJShM2p0WiwadMmaWVtbGwM
GRkZ8PPzQ3x8PIKDg2E2m6XTakUWbRqNBunp6YiPj5eaS8+cOYMLFy4gLS1NWrUEgB9++OF/m7Pv
paeeegrl5eVQq9U3vMSCXq9HeXm5Tc+CZHPpLHD27Fk0NTWhq6sL/f390nU8vL29sWDBArzwwgs2
6VW4cuUKDAYDfHx8ZtSpWsD4p+LDhw9jw4YNCAsL+984s9mM3bt3o6urC6WlpUJy++2339Db24ul
S5feMO6vv/7Czp07ERMTY9H/YSs6nQ56vR5BQUHw8PAQPn97e7vFmJOTE8LDwyeNGQwG5OXlQa1W
C/3jOWF4eBj19fVoa2uDTqfDyMiIdO2dkJAQREdH44knnhCeV2FhIRITE23yfnEr/vjjD9TV1WFk
ZAQLFy7E4sWLAQCNjY2orKzEn3/+iYCAAGzatAkRERFCczt//jxKSkpw+vRpmEwmPPLII0hKSkJi
YuKkuI6ODvj4+Ag9mwoAenp6kJ6eDqPRiOeffx6hoaHw9vaGk5MTTCYT+vv7ce7cOZw8eRIymQwH
DhzAo48+KjTHCSw8iIiI7gN6vR6HDh3C8ePHMTAwYPG4p6cnVqxYgbS0NMybN88GGY5j4UFERHSf
6evrs1ght3Uz8wQWHkRERA8QW9/CYmZc15WIiIiEKC8vx5o1a2w2PwsPIiIiEmZmnYpARERE0zad
W1j88ssv9zCTm2OPBxER0Sz37LPPTvsWFiLvyH09rngQERHNcjP5FhZTsfAgIiKa5WbyLSymYnMp
ERHRLKdUKtHb22v1wmFTib6FxVTs8SAiIprlZvItLKZi4UFERETCcKuFiIiIhGHhQURERMKw8CAi
IiJhWHgQ0X3n4sWLiIyMRE1Nja1TIaIpZnbrKxHdN2pqalBYWCgdOzg4QKFQICoqChqNBg8//PC0
X7OhoQEDAwNYt27d3UyViO4hFh5EJFRGRgb8/Pxw9epVnDlzBrW1tTh9+jSOHDkCFxeXab1WQ0MD
uru7LQoPX19ftLS0zPjTCokeRPytJCKhlixZgtDQUABAfHw8PDw8cPjwYZw4cQIrV668K3PY2dlN
u4ghIjHY40FENhUREQEA+P3336Wx5uZmZGVlYfXq1Vi8eDFeeuklHDx4EKOjo1LMli1bcPLkSfT2
9iIyMhKRkZGIi4sDYL3Ho6CgACqVCnq9Hjk5OVCpVIiOjkZxcfGk1wUAg8GAd999F8uXL4darUZ+
fj66urrYN0J0F3DFg4hs6uLFiwDGL+M8oba2FnK5HOvXr8ecOXPw448/4pNPPsHw8DCysrIAAJs3
b8bQ0BD0ej2ys7MBAHK5/IZzmc1mvPHGG3jyySeRlZWF1tZWaLVa+Pv7IykpSYrJzs7Gzz//jMTE
RAQGBuK7775DQUHBPfjuiR48LDyISKihoSEYDAYYjUacPXsWn376KZydnaFSqaSY999/HzKZTDpO
SkrCzp07UVFRga1bt8LZ2RmLFi1CeXk5Ll++jNjY2Fua22g0IiYmBunp6dLrrl+/HtXV1VLh0dzc
jM7OTuTk5CA1NVWKy8zMvFs/AqIHGgsPIhJKo9FMOvbz88N7772HefPmSWPXFx3Dw8MwmUyIiIhA
VVUVenp6sGDBgtuePzExcdJxREQEvv76a+n41KlTcHR0REJCgjRmb2+P5ORktLW13fa8RDSOhQcR
CZWbm4uAgAAMDQ3hq6++QkdHB5ycnCbFdHd3o6SkBG1tbRgeHp702NDQ0G3P7eLiAk9Pz0ljbm5u
+Pvvv6Xj3t5eeHt7Typ+AGD+/Pm3PS8R/YeFBxEJpVQqpbNa1Go10tPTsWPHDlRWVkIul+Py5cvY
smULXF1dkZGRAX9/fzg7O+P8+fPYu3cvzGbzbc9tb89+eiJb428hEdmMg4MDMjMz0dfXhy+++AIA
0N7ejsHBQeTn5yM1NRUqlQpRUVFwd3e3eL6dnd1dz8nX1xf9/f34559/Jo3rdLq7PhfRg4iFBxHZ
VGRkJJRKJcrKymA0GqVVibGxMSnGZDKhoqLC4rkymeyOtl6sWbRoEa5du4Yvv/xSGjObzVbnJ6Lp
41YLEdncxo0bsX37dtTU1CA6Ohru7u4oKChASkoK7OzsJjV/Xi8kJATHjh1DUVERQkNDIZfLsWzZ
sjvKRa1WQ6lUori4GDqdDoGBgThx4gQGBwcB3JtVFqIHCVc8iMjmVqxYAX9/f2i1Wri5uWH37t3w
9vZGSUkJtFotoqKisG3bNovnJScnY/Xq1aipqcGOHTuwa9euO87FwcEBe/bswcqVK1FXV4f9+/dD
oVDgnXfeAQA4Ozvf8RxEDzK7sevXM4mIyKrm5ma8/fbbOHjwIJ5++mlbp0M0a3HFg4hoiqmNpaOj
ozhy5Ajmzp2L4OBgG2VFdH9gjwcR0RS7du2C0WhEWFgYTCYTvv32W3R2diIzM9Pi+h5END3caiEi
mqKhoQFarRY6nQ5Xr17F/PnzkZiYiJSUFFunRjTrsfAgIiIiYdjjQURERMKw8CAiIiJhWHgQERGR
MCw8iIiISBgWHkRERCQMCw8iIiIShoUHERERCcPCg4iIiIRh4UFERETC/AugXWBUhAYZoAAAAABJ
RU5ErkJggg==
"
>
</div>

</div>

</div>
</div>

</div>
    </div>
  </div>
</body>

 


</html>

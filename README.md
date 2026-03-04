# AO3-Ros-Pine-sunset
Customization of the Rosé Pine Moon_Card skin by BlackBatCat for AO3
# AO3-May-Skin

This is a customization of the **Rosé Pine Moon_Card** skin by **BlackBatCat** for Archive of Our Own (AO3).  
It modifies titles, authors, fandoms, warnings, dates, and tags layout to match a personal style preference.

## Files included

- `Rosé Pine - Base.ketty.css`
- `Rosé Pine - Moon.ketty.css`
- `Rosé Pine - Tag sunset.ketty.css`
- `Rosé Pine - Tablet.ketty.css`
- `Mobile Skin.ketty.css`
- `May-Skin-Custom.css` — your personal modifications

/* ==========================================
   Nome file: Rosé Pine - Base.ketty.css
   Autore originale: BlackBatCat
   Tipo: Skin base AO3
   Descrizione: Base della skin Rosé Pine
   ========================================== */
   
  body {
  font-size: var(--txt-size-main);
  color: var(--txt-main);
}

#outer {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  background-color: var(--bg1);
}

#inner {
  flex-grow: 1;
  display: flex;
  flex-flow: row;
  justify-content: flex-start;
  min-height: 70vh;
}

.blurb li,
.meta ul li {
  padding-left: 0;
}

a:active,
a:focus,
a:focus img,
button:focus,
#footer a:focus,
#footer button:focus,
.submit input:focus,
.filters input:focus+.indicator+span,
.filters .expander:focus {
  outline: none;
}

a,
a:link,
a.work,
.blurb h4 a:link,
div.preface .byline a,
.filters p a {
  border-bottom: var(--link-underline);
  color: var(--link);
}

a:is(:hover,
:focus),
a:visited:is(:hover,
:focus),
.blurb .heading a:is(:hover,
:focus),
.blurb .heading a:visited:is(:hover,
:focus),
div.preface .byline a:is(:hover,
:focus),
.fandom.index.group a.tag:is(:hover,
:focus),
h2.heading a.tag:is(:hover,
:focus),
.filters p a:is(:hover,
:focus) {
  border-bottom-color: inherit;
  color: var(--link-hgl);
}

a:visited,
.blurb .heading a:visited {
  color: var(--link-visited);
}

a img {
  border: none;
}

h2 {
  font-size: 1.8em;
  line-height: 1.2;
}

h2.heading:has(+ .navigation.actions.module) {
  display: block;
  margin-top: 0;
}

hr {
  border: none;
  border-bottom: 3px double;
}

em,
cite,
i {
  font-style: italic;
}

table {
  border: var(--border-width) solid var(--border2);
  background-color: var(--bg4);
}

thead,
tfoot,
tbody tr {
  border-color: var(--border2);
}

thead th {
  border-color: var(--border2);
  background-color: var(--bg1);
}

thead td {
  border-color: var(--bg4);
  background-color: var(--border1);
}

tbody th {
  border-color: var(--border2);
  background-color: var(--bg1);
}

tfoot td {
  border-color: var(--border4);
}

td {
  padding: 0.25em 0.5em;
}

tr:hover,
col.name {
  border-color: var(--border2);
  background: var(--bg5);
}

#header,
#tos_prompt .heading {
  display: flex;
  flex-wrap: wrap;
  align-items: flex-start;
  align-content: center;
  column-gap: 1.25em;
  position: unset;
  z-index: 100;
  box-sizing: border-box;
  width: 96%;
  max-width: 96%;
  margin-top: 2%;
  margin-right: 2%;
  margin-bottom: 0;
  margin-left: 2%;
  border-width: var(--border-width);
  border-style: solid;
  border-color: var(--border1);
  border-radius: var(--radius-mid);
  box-shadow: var(--shadow-header);
  background: var(--bg2);
}

#header>h1,
#header>h2,
#header>nav .user,
#header>nav .dropdown-toggle,
#header li.search {
  display: flex;
  align-items: center;
  box-sizing: border-box;
  min-height: 38px;
}

#header div.clear {
  display: none;
}

#header .heading {
  order: 1;
  margin-left: var(--margins-header);
  padding: 0;
}

#header .heading a {
  font-size: 1em;
  line-height: 1;
}

#header .heading a::before {
  font-weight: var(--txt-bold);
  font-size: 1.15em;
  color: var(--txt-header);
}

#header .heading a:is(:hover,
:focus)::before {
  -webkit-background-clip: text;
  background-image: var(--txt-header-hgl-h1);
  color: transparent;
}

#header .heading a * {
  display: none;
}

#header .dropdown-menu,
#small_login {
  z-index: 5;
  box-sizing: border-box;
  width: unset;
  min-width: 15em;
  padding: 0.25em 0;
  border: 1px solid var(--border3);
  border-radius: var(--radius-mid);
  box-shadow: var(--shadow);
  background: var(--bg6);
  font-size: 0.95em;
}

#header nav:not(:has(.open)) li.dropdown:hover::before,
#header .open::before {
  position: absolute;
  z-index: 6;
  width: 0;
  height: 0;
  border-right: 8px solid transparent !important;
  border-bottom: 8px solid var(--bg6);
  border-left: 8px solid transparent !important;
  color: var(--border3);
  transform: translate(-50%, 31px);
  filter: drop-shadow(0 -1px);
  content: "";
}

#greeting .dropdown-menu {
  z-index: 7;
  transform: translateX(1.5em);
}

#header #greeting:not(:has(.open)) li.dropdown:hover::before,
#header #greeting .open::before {
  z-index: 8;
  transform: translate(5%, 31px);
}

#header .navigation .dropdown .menu li {
  margin: 0 0.25em;
  border-bottom: none;
  text-align: left;
}

#header .navigation .dropdown:is(*) .menu li a {
  display: block;
  max-width: unset;
  padding: 0.5em;
  border-radius: var(--radius-small);
  background-color: transparent;
  color: var(--txt-main);
  transition: 25ms ease-out;
}

#header .navigation .dropdown .menu li a:is(:hover,
:focus) {
  background: var(--int-hgl-bg);
  color: var(--int-hgl-txt);
}

#header .navigation a,
#header .user a {
  background: transparent;
  color: var(--txt-header);
}

#header .navigation.actions .dropdown:is(.open,
:hover,
:focus,
:active)>a,
#header .navigation.actions>.dropdown a:is(:hover,
:focus,
:active),
#header .user a:is(:hover,
:focus,
:active) {
  background: transparent;
  color: var(--txt-header-hgl);
}

#login,
#greeting {
  order: 3;
  width: auto;
  margin-right: var(--margins-header);
  margin-left: auto;
  background-color: transparent;
}

#header .user,
#header .user a,
#small_login .action,
#greeting .user>li {
  margin: 0;
  padding: 0;
}

#greeting .user>li {
  line-height: 0;
}

#greeting p.icon {
  display: none;
}

#header #greeting .dropdown>a[href*="/users/"] {
  content: url("https://wolfbatcat.github.io/ao3-rose-pine/assets/zerafina-header-icon-user.png");
}

#header #greeting .dropdown>a[href*="/works/new"] {
  content: url("https://wolfbatcat.github.io/ao3-rose-pine/assets/zerafina-header-icon-new-work.png");
}

#header #greeting a[href*="/users/logout"] {
  content: url("https://wolfbatcat.github.io/ao3-rose-pine/assets/zerafina-header-icon-logout.png");
}

#header #greeting>ul>li>a {
  display: inline-block;
  height: 18px;
  padding: 10px 0;
  background: transparent;
  filter: var(--header-icon);
}

#header #greeting>ul>li:is(.open,
:hover,
:focus)>a,
#header #greeting>ul>li>a:is(:hover,
:focus) {
  filter: var(--header-icon-hgl);
}

#header>nav .user {
  column-gap: 0.5em;
}

#header nav:has(> .primary) {
  order: 2;
  flex: 1;
  max-width: 100%;
  border-width: var(--border-width) !important;
  border-color: var(--border2) !important;
}

#header .primary {
  display: flex;
  flex-wrap: wrap;
  justify-content: left;
  align-content: center;
  align-items: center;
  box-sizing: border-box;
  box-shadow: none;
  background: none;
}

#header .primary>li.dropdown:first-of-type {
  margin-left: 0;
}

#header .search {
  margin: 0;
}

#header li.search {
  margin-inline: 1.25em;
}

#header li.search::before {
  position: absolute;
  left: 0.4em;
  z-index: 1;
  font-weight: var(--txt-bold);
  font-size: 1.25em;
  color: var(--link-hgl);
  content: "\002315";
}

#header li.search form label {
  display: none;
}

#header #search .text {
  min-width: 170px;
  max-width: 20vw;
  margin: 0;
  padding-left: 1.8em;
  border: var(--border-width) solid var(--border2);
  border-radius: var(--radius-alt);
  box-shadow: none;
  background-color: var(--int-search);
  transition: width 0.15s;
}

#header #search input:focus {
  color: var(--txt-main);
  border-color: var(--int-hgl);
  outline: 1px solid var(--int-hgl);
}

#header #search .button,
#header #search span.actions {
  display: none;
}

#header h2 {
  order: 4;
  display: block;
  width: 100%;
  min-height: unset;
  max-height: 30vh;
  padding: 0.25em var(--margins-header);
  border-inline: none;
  border-top: var(--border-width) solid var(--border2);
  border-bottom-left-radius: var(--radius-big);
  border-bottom-right-radius: var(--radius-big);
  background-color: var(--link-hgl) !important;
  background-size: auto 100% !important;
  font-size: 1.15em;
  font-weight: bold;
  color: var(--int-hgl-txt);
}

#dashboard,
#dashboard.own {
  position: sticky;
  top: 1em;
  box-sizing: border-box;
  width: 18%;
  min-width: 150px;
  max-width: 230px;
  max-height: 96vh;
  overflow-x: visible;
  overflow-y: auto;
  margin-top: 1.85em;
  margin-left: 2%;
  padding-top: 0.429rem;
  padding-right: 0.5rem;
  padding-bottom: 0.5rem;
  padding-left: 0.5rem;
  border-width: var(--border-width);
  border-style: solid;
  border-color: var(--border1) !important;
  border-radius: var(--radius-mid);
  background-color: var(--bg5);
  font-size: 0.875em;
  scrollbar-color: transparent transparent;
  box-shadow: var(--shadow-header);
}

#dashboard ul {
  display: block;
  float: none;
  position: relative;
  padding-top: 0.429em;
  padding-bottom: 0.429em;
  border-top-width: var(--border-width);
  border-top-style: solid;
  border-top-color: var(--border1);
  text-align: left;
}

#dashboard ul:not(.secondary):first-of-type {
  border-top: 0;
}

#dashboard a,
#dashboard span {
  display: block;
  box-sizing: border-box;
  max-width: 100%;
  margin-block: 1px;
  padding-top: 0.429em;
  padding-right: 0.5rem;
  padding-bottom: 0.429em;
  padding-left: 0.5rem;
  border-radius: var(--radius-small);
  color: var(--txt-main);
  line-height: 1.286;
}

#dashboard a:is(:hover,
:focus) {
  background: var(--int-hgl-bg);
  color: var(--int-hgl-txt);
}

#dashboard .current {
  background-color: var(--int-current-bg);
  color: var(--int-current-txt);
  border-width: 1px;
  border-style: solid;
  border-color: var(--int-current-border);
  box-shadow: var(--shadow-box2);
  font-weight: var(--txt-semibold);
}

#dashboard .current:hover {
  font-weight: var(--txt-bold);
  box-shadow: none;
}

#dashboard .secondary {
  margin-block: 0.25em;
  padding: 0.25em;
  border-width: var(--border-width);
  border-style: solid;
  border-color: var(--border3);
  box-shadow: var(--shadow);
  background-color: var(--bg6);
}

#main,
#main.dashboard {
  flex-grow: 1;
  box-sizing: border-box;
  min-height: unset;
  max-width: 100%;
  margin: 0;
  padding: 1.5em var(--margins-main);
  line-height: 1.286;
}

#main.dashboard {
  width: 82%;
}

#main.errors,
#main.error-502,
#main.error-503-maintenance,
#main.session {
  background: none;
}

#main.errors p,
#main.errors .heading {
  margin-right: 0;
}

#main.errors h2.heading::before {
  display: inline-block;
  width: 1em;
  height: 1em;
  margin-right: 0.5em;
  padding: 0.1em;
  border-radius: 100%;
  background-color: var(--alert-txt);
  line-height: 1;
  text-align: center;
  color: var(--txt-alt2);
  content: "!";
}

#footer {
  box-sizing: border-box;
  width: 100%;
  max-width: 100%;
  padding: 3% 5%;
  margin-top: 2%;
  border-top: var(--border-width) solid var(--border2);
  background: linear-gradient(to top, var(--bg1) 70%, var(--bg2) 100%);
  overflow: hidden;
  overflow-wrap: anywhere;
  font-size: 0.8em;
  word-break: normal;
  color: var(--txt-main);
}

#footer ul.navigation.actions {
  display: flex;
  justify-content: space-between;
  column-gap: 5%;
  box-sizing: border-box;
  width: 100%;
  margin: 0;
  padding: 0;
}

#footer ul li.module {
  box-sizing: border-box;
  max-width: unset;
  margin: 0;
  padding: 0;
}

#footer ul li.module ul.menu {
  display: block;
  float: unset;
}

#footer .heading {
  margin-block: 0 1em;
  font-weight: var(--txt-bold);
  color: var(--txt-main);
}

#footer a,
#footer button {
  border-bottom: var(--link-underline) !important;
  text-decoration: none;
  color: var(--link);
}

#footer a:is(:hover,
:focus),
#footer button:is(:hover,
:focus) {
  border-bottom-color: inherit !important;
  color: var(--link-hgl);
}

fieldset,
form dl,
fieldset dl dl,
fieldset fieldset fieldset,
fieldset fieldset dl dl,
dd.hideme,
form blockquote.userstuff,
form.single fieldset {
  margin: 0.643em 0;
  padding: 0.634em;
  border: var(--border-width) solid var(--border2);
  border-radius: var(--radius-big);
  box-shadow: var(--shadow-box2);
  background-color: var(--bg4);
}

fieldset dl,
fieldset.actions,
fieldset dl fieldset dl {
  border: none;
  background-color: transparent;
}

fieldset fieldset {
  background-color: var(--bg4);
}

fieldset dd dl,
form .meta dd,
fieldset dl fieldset dl,
dd fieldset {
  margin: 0.643em 0;
}

label {
  margin-right: 0;
}

fieldset>fieldset>dl>dt>label {
  font-weight: var(--txt-bold);
}

fieldset>ul>li:has(label input[type="radio"]) {
  margin: 0 !important;
}

input,
input[type="number"],
textarea {
  box-sizing: border-box;
  width: 100%;
  max-width: 100%;
  border: var(--border-width) solid var(--border2);
  border-radius: var(--radius-mid);
  box-shadow: none;
  background-color: var(--bg5);
  color: var(--txt-main);
}

textarea {
  border-radius: var(--radius-big);
}

input[type="text"]:focus,
input[type="number"]:focus,
.search input[type="text"]:focus,
input#user_password:focus,
select:focus,
textarea:focus {
  border-color: var(--int-hgl);
  outline: 1px solid var(--int-hgl);
  background-color: var(--int-bg);
}

select {
  width: 100%;
  min-width: 10.5em;
  padding: 0.25em;
  border: var(--border-width) solid var(--border2);
  border-radius: var(--radius-small);
  background-color: var(--bg5);
  font-size: 0.95em;
  vertical-align: middle;
  color: var(--txt-main);
}

select:not(select[multiple]):is(:hover,
:focus) {
  background: var(--bg5);
}

select:not(select[multiple]):open {
  background: var(--bg6);
}

.datetime select {
  width: fit-content;
}

option,
.actions option,
form code {
  color: var(--txt-main);
}

option {
  margin: 0;
  padding: 0.125em;
  border-radius: var(--radius-small);
}

option:is(:hover,
:focus,
:active) {
  background: var(--int-hgl-bg);
  color: var(--int-hgl-txt);
}

option:is(:checked),
option:checked:is(:hover,
:focus,
:active) {
  background: var(--int-current-bg);
  color: var(--int-current-txt);
}

form dt {
  display: inline-block;
  box-sizing: border-box;
  width: 25%;
  min-width: unset;
  border-bottom: var(--border-width) solid var(--border2);
}

form dd,
form dd.any {
  box-sizing: border-box;
  width: 75%;
}

form dd+dd {
  width: 100%;
}

form dd.required {
  color: var(--txt-main);
}

form fieldset#parent-options dd:has(ul) {
  margin: 0;
}

form.verbose legend,
.verbose form legend,
form.single legend {
  border: var(--border-width) solid var(--border2);
  border-radius: var(--radius-small);
  box-shadow: var(--shadow-box2);
  background-color: var(--bg6);
  font-weight: var(--txt-bold);
}

dt.warning {
  font-weight: 400;
}

dt.warning>a:nth-child(1) {
  color: var(--txt-main);
}

input[type="checkbox"],
input[type="radio"],
.filters [type="radio"],
.filters [type="checkbox"],
.actions input[type="checkbox"],
label.action input[type="checkbox"] {
  flex-shrink: 0;
  appearance: none;
  display: inline-block;
  position: relative;
  top: 0.1em;
  box-sizing: border-box;
  width: 1em;
  height: 1em;
  margin: 0;
  box-shadow: none;
  border: 1.5px solid var(--border2);
  border-radius: var(--radius-small);
  background-color: var(--bg5);
  background-image: none !important;
  color: var(--txt-alt2);
  user-select: none;
}

input[type="checkbox"]:hover,
input[type="radio"]:hover,
.actions input[type="checkbox"]:hover,
label.action input[type="checkbox"]:hover,
.filters [type="checkbox"]:hover:not(:checked)::before {
  border-color: var(--int-hgl);
  color: var(--int-hgl);
}

input[type="checkbox"]:disabled,
input[type="radio"]:disabled {
  border-color: var(--int-disabled) !important;
  background-color: var(--int-disabled) !important;
  cursor: not-allowed;
}

input[type="radio"]+label,
input[type="checkbox"]+label {
  padding-left: 0;
}

ul:not(ul.actions) li:has(input[type="checkbox"] + label):not(:has(fieldset)),
ul:not(ul.actions) li:has(input[type="radio"] + label):not(:has(fieldset)),
ul:not(ul.actions) li:not(.blurb ul li)>label:has(input[type="checkbox"]),
ul:not(ul.actions) li:not(.blurb ul li)>label:has(input[type="radio"]) {
  display: flex !important;
  align-items: baseline;
  column-gap: 0.5em;
  width: fit-content;
  margin: 0;
  padding-block: 0.3215em;
}

input[type="checkbox"]:checked,
.actions input[type="checkbox"]:checked,
label.action input[type="checkbox"]:checked {
  border-color: var(--int-checked);
  background-color: var(--int-checked);
  color: var(--txt-alt2);
}

input[type="checkbox"]::before,
.filters [type="checkbox"]::before,
.actions input[type="checkbox"]::before {
  position: absolute;
  width: 50%;
  height: inherit;
  border-right: 0.25em solid;
  border-bottom: 0.25em solid;
  color: var(--txt-alt2);
  content: "";
  transform: translate(15%, -20%) scale(0.5) rotate(45deg);
  opacity: 0;
}

.filters .exclude [type="checkbox"]::before {
  width: 100%;
  border: none;
  font-size: 0.75em;
  line-height: 1;
  text-align: center;
  content: "\002716\fe0e";
  transform: unset;
}

input[type="checkbox"]:checked::before,
.filters [type="checkbox"]:checked::before,
.actions input[type="checkbox"]:checked::before {
  opacity: 1;
}

.filters [type="checkbox"]:not(:checked)::before {
  color: var(--border2);
  opacity: 1;
}

input[type="checkbox"]:checked:hover,
.actions input[type="checkbox"]:checked:hover,
label.action input[type="checkbox"]:checked:hover {
  border-color: var(--int-hgl);
  background-color: var(--int-hgl);
}

.actions input[type="checkbox"] {
  vertical-align: baseline;
}

.filters [type="radio"]+.indicator,
.filters [type="checkbox"]+.indicator {
  display: none;
}

input[type="radio"],
.filters [type="radio"] {
  border-radius: 100%;
}

input[type="radio"]:checked,
.filters [type="radio"]:checked {
  border-color: var(--int-checked);
  box-shadow: inset 0 0 0 2.5px;
  background-color: var(--int-checked);
  background-image: none;
  color: var(--int-bg);
}

input[type="file"] {
  background: transparent;
}

input::file-selector-button {
  box-shadow: none !important;
}

p.character_counter {
  font-size: 0.85em;
}

.LV_validation_message {
  display: block;
}

.LV_invalid {
  border: var(--border-width) solid var(--alert-txt);
  border-radius: var(--radius-big);
  color: var(--alert-txt);
  background: var(--alert-bg);
  box-shadow: none;
}

.LV_invalid_field,
input.LV_invalid_field:is(:hover,
:focus),
textarea.LV_invalid_field:is(:hover,
:focus) {
  border: var(--border-width) solid var(--alert-txt);
}

.LV_invalid::before {
  border-color: var(--alert-txt) transparent;
}

.autocomplete div.dropdown {
  background: transparent;
}

.autocomplete div.dropdown ul {
  padding: 0.125em;
  border: 1px solid var(--border4);
  border-radius: var(--radius-small);
  box-shadow: var(--shadow);
  background: var(--bg6);
  color: var(--txt-main);
}

.autocomplete .dropdown ul li {
  margin: 0.125em;
  padding: 0.25em;
  border-radius: var(--radius-small);
}

.autocomplete .dropdown ul li:is(:hover,
:focus),
.autocomplete .dropdown li.selected {
  background: var(--int-hgl-bg);
  color: var(--int-hgl-txt);
}

.required .autocomplete {
  color: var(--txt-main);
}

.autocomplete .notice {
  border: 1px solid var(--border4);
  border-radius: var(--radius-small);
  box-shadow: var(--shadow);
  background: var(--bg6);
  font-size: 0.95em;
  color: var(--txt-main);
}

.ui-sortable li,
.ui-sortable li:is(:hover,
:focus) {
  border: var(--border-width) solid var(--border1);
  border-radius: var(--radius-small);
  box-shadow: none;
  background: var(--bg4);
}

.ui-sortable li:hover:not(.ui-sortable ul.actions li:hover),
.ui-draggable form {
  box-shadow: var(--shadow);
}

#ui-datepicker-div {
  border: var(--border-width) solid var(--border4);
  border-radius: var(--radius-mid);
  box-shadow: var(--shadow);
  background: var(--bg6);
}

.ui-datepicker-header a {
  cursor: pointer;
}

.ui-datepicker table {
  background: var(--bg4);
}

.ui-datepicker td {
  border-color: var(--border2);
}

.ui-datepicker tr:hover {
  background: var(--border1);
}

.ui-datepicker td:hover {
  background: var(--bg1);
}

.search [role="tooltip"],
.qtip-content {
  z-index: 6;
  padding: 0.429em;
  border: 1px solid var(--border4);
  border-radius: var(--radius-small);
  box-shadow: var(--shadow);
  background: var(--bg6);
  color: var(--txt-main);
}

.qtip-content {
  border-top-left-radius: 0;
  font-size: 1.15em;
}

#modal {
  border: var(--border-width) solid var(--border3);
  border-radius: var(--radius-big);
  box-shadow: none;
  background: var(--bg4);
}

#modal .content {
  border-bottom: var(--border-width) solid var(-

/* ==========================================
   Nome file: Rosé Pine - Moon.ketty.css
   Autore originale: BlackBatCat
   Tipo: Skin AO3
   Descrizione: Modifiche della variante “Moon” della skin Rosé Pine
   ========================================== */

:root {
  --margins-header: 1rem;
  --margins-main: 5%;
  --margins-narrow: 2.5%;
  --radius-small: 0.75rem;
  --radius-mid: 0.75rem;
  --radius-big: 0.75rem;
  --radius-alt: 0.75rem;
  --radius-tag: 0 15px 15px;
  --icon-content-radius: 0.75rem;
  --icon-primary-radius: 50%;
  --icon-index-radius: 0.75rem;
  --bg1: #232136;
  --bg2: #2a273f;
  --bg3: #232136;
  --bg4: var(--bg5);
  --bg5: var(--bg2);
  --bg6: var(--bg5);
  --bg7: var(--bg5);
  --border1: #36324e;
  --border2: #3f3857;
  --border3: var(--border2);
  --border4: #463e61;
  --border-width: 1px;
  --shadow: 0 0.2em 0.4em rgba(25, 22, 37, 0.25);
  --shadow-header: var(--shadow-box1);
  --shadow-buttons: 0 3px 8px 0 rgba(35, 33, 54, 0.33), 0 2px 0 0 rgba(100, 90, 120, 0.15);
  --shadow-box1: 0 8px 28px 0 rgba(35, 33, 54, 0.60), 0 4px 0 0 rgba(35, 33, 54, 0.32);
  --shadow-box2: 0 3px 10px 0 rgba(35, 33, 54, 0.28), 0 2px 0 0 rgba(35, 33, 54, 0.17);
  --txt-size-main: 115%;
  --txt-size-work: 140%;
  --txt-header: #e0def4;
  --txt-header-hgl: var(--link-hgl);
  --txt-header-hgl-h1: linear-gradient(125deg, #ebbcba, #eb6f92);
  --txt-main: var(--txt-header);
  --txt-alt1: #FFFFFF;
  --txt-alt2: #FFFFFF;
  --txt-semibold: 600;
  --txt-bold: 700;
  --link: #eb6f92;
  --link-hgl: #eb6f92;
  --link-visited: #9ccfd8;
  --link-underline: 1px solid transparent;
  --int-btn-bg: #2e2c44;
  --int-btn-border: var(--border4);
  --int-btn-txt: var(--txt-main);
  --int-btn-hgl-bg: linear-gradient(to bottom right, #ebbcba 0%, #ea9a97 33%, #eb6f92 100%);
  --int-btn-hgl-txt: var(--txt-alt2);
  --int-btn-hgl-border: #00000020;
  --int-bg: var(--bg5);
  --int-search: #28253c;
  --int-current-bg: #34304f;
  --int-current-txt: var(--txt-main);
  --int-current-border: var(--tag-border);
  --int-disabled-bg: var(--border1);
  --int-checked: #eb6f92;
  --int-hgl: var(--link-hgl);
  --int-hgl-bg: var(--int-btn-hgl-bg);
  --int-hgl-txt: var(--txt-alt2);
  --icon-content-complete: #3e8fb0;
  --icon-content-incomplete: #9ccfd8;
  --icon-content-public: #3e8fb0;
  --icon-content-private: #eb6f92;
  --icon-content-hidden: #908caa;
  --icon-content-rec: #ebbcba;
  --icon-rating-gen: #9ccfd8;
  --icon-rating-teen: #3e8fb0;
  --icon-rating-mature: #ebbcba;
  --icon-rating-explicit: #eb6f92;
  --icon-relationship-mm: #eb6f92;
  --icon-relationship-mf: #3e8fb0;
  --icon-relationship-gen: #9ccfd8;
  --icon-relationship-ff: #ebbcba;
  --icon-multi: conic-gradient(from 360deg, #eb6f92 0% 25%, #9ccfd8 25% 50%, #ebbcba 50% 75%, #3e8fb0 75% 100%);
  --icon-relationship-other: linear-gradient(to left top, #3e8fb0, #9ccfd8, #eb6f92, #ebbcba);
  --icon-warning-choose-not: #9ccfd8;
  --icon-warning-yes: #eb6f92;
  --icon-content-external: #ebbcba;
  --icon-bg: var(--int-bg);
  --icon-id: var(--link);
  --icon-anon: var(--border4);
  --icon-border1: var(--int-btn-hgl-border);
  --icon-border2: var(--border2);
  --tag-default-bg: #393757;
  --tag-fandom-bg: #eb6f92;
  --tag-warning-bg: #ebbcba;
  --tag-ship-bg: #9ccfd8;
  --tag-character-bg: #3e8fb0;
  --tag-freeform-bg: var(--tag-default-bg);
  --tag-splash-bg: var(--bg5);
  --tag-default-txt: var(--txt-alt1);
  --tag-fandom-txt: var(--txt-alt1);
  --tag-warning-txt: var(--txt-alt1);
  --tag-ship-txt: var(--txt-alt1);
  --tag-character-txt: var(--txt-alt1);
  --tag-freeform-txt: var(--txt-alt1);
  --tag-border: #9893a525;
  --tag-hgl-bg: var(--int-btn-hgl-bg);
  --tag-hgl-txt: var(--txt-alt2);
  --tag-hsl-shadow: inset 0 0 0 1px rgba(255,255,255,0.3);
  --notice-bg: #1a2630;
  --success-bg: #162a2c;
  --caution-bg: #2a203a;
  --alert-bg: #2a1820;
  --notice-txt: #9ccfd8;
  --success-txt: #3e8fb0;
  --caution-txt: #c4a7e7;
  --alert-txt: #eb6f92;
  --header-icon: brightness(0) saturate(100%) invert(88%) sepia(20%) saturate(167%) hue-rotate(206deg) brightness(97%) contrast(96%);
  --header-icon-hgl: brightness(0) saturate(100%) invert(62%) sepia(26%) saturate(1195%) hue-rotate(299deg) brightness(90%) contrast(105%);
  --kudos-icon: var(--header-icon);
  --lock-icon: var(--header-icon);
  --tag-filter: brightness(1.10);
  --stats-icon: var(--header-icon);
  --stat-chart: invert(96%) saturate(20%) hue-rotate(75deg) brightness(115%);
  --rich-txt-editor: none;
}

body,
input,
.toggled form,
.dynamic form,
.secondary,
.dropdown,
blockquote,
.prompt .blurb h6,
.bookmark .user .meta,
a.work,
span.symbol,
.heading .actions,
.heading .action,
.heading span.actions,
button,
span.unread,
.replied,
span.claimed,
.actions span.defaulted,
.splash .news .meta,
.datetime,
h5.fandoms.heading a.tag,
dd.fandom.tags a,
select {
  font-family: Figtree, Bitter, Helvetica, "Trebuchet MS", "Lucida Sans", Arial, sans-serif, "GNU Unifont";
}

h1,
h2,
h3,
h4,
h5,
h6,
.heading {
  font-family: Figtree, Bitter, Helvetica, "Trebuchet MS", "Lucida Sans", Arial, sans-serif, "GNU Unifont";
  font-weight: var(--txt-bold);
}

kbd,
tt,
code,
var,
pre,
samp,
textarea,
textarea#skin_css,
.css.module blockquote pre,
#floaty-textarea {
  font-family: Victor Mono Medium, Consolas, Monaco, Courier, monospace;
  font-size: 0.9em;
}

#header .heading a::before {
  content: "Archive of Our Own\00a0✿";
}

#dashboard .current:after {
  content: "\00a0✿";
}

.home .header h2::after {
  content: "\00a0✿";
}

.splash>.module h3::after {
  content: "\00a0✿";
}

a.tag:not(.fandom.index.group a.tag,
h2.heading a.tag,
.splash .favorite a.tag,
h5.fandoms.heading a.tag,
dd.fandom.tags a,
[class^=warning] a.tag,
[class^=relationship] a,
[class^=character] a.tag):after {
  content: "\00a0\00a0✿";
}

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ body .blurb {
  display: flex !important;
  flex-direction: column !important;
}

body .blurb .header .heading {
  order: 1 !important;
}

body .blurb .header .heading + span.byline {
  order: 2 !important;
}

body .blurb ul.fandom.tags {
  order: 3 !important;
}

+++++++++++++++++++++++++++++++++++++++ body .blurb:has(a.tag.complete-yes) h4.heading a[href*="/works/"] {
  color: #648a82 !important;
}

body .blurb:has(a.tag.complete-yes) h4.heading:not(:has(a[href*="/works/"])) {
  color: #648a82 !important;
}

body .blurb:has(.required-tags .complete-yes) {
  border: 1px solid palevioletred !important;
  padding-left: 0.75em !important;
  box-shadow: 0 0 8px rgba(255, 218, 185, 0.45) !important;
}

*************************************** body .blurb ul.fandom.tags {
  display: block !important;
  width: 100% !important;
  clear: both !important;
  float: none !important;
  margin-top: 0.35em !important;
}

body .blurb ul.fandom.tags li,
body .blurb ul.fandom.tags a.tag {
  float: none !important;
  clear: both !important;
  white-space: nowrap !important;
}

body .blurb ul.fandom.tags[style*="display: none"],
body .blurb ul.fandom.tags.hidden {
  float: none !important;
  clear: both !important;
  width: 100% !important;
}

. .actions a[href*="/chapter/next"],
.actions a[href*="/chapter/next"]:link,
.actions a[href*="/chapter/next"]:visited,
.actions button[name="next_chapter"],
.actions button[name="next_chapter"]:link,
.actions button[name="next_chapter"]:visited {
  background: var(--int-btn-hgl-bg) !important;
  color: var(--int-btn-hgl-txt) !important;
  border: 1px solid var(--int-btn-border) !important;
}

/* ==========================================
   Nome file: Rosé Pine - Tag sunset.ketty.css
   Autore originale: BlackBatCat
   Tipo: Skin AO3
   Descrizione: Stile personalizzato per i tag con tema “Sunset”
   ========================================== */

:root {
  --tag-default-txt: #908CAA;
  --tag-fandom-txt: #90233E;
  --tag-warning-txt: #B93957;
  --tag-ship-txt: #F26D85;
  --tag-platonic-ship-txt: #E78E9F;
  --tag-character-txt: #F2C7CB;
  --tag-freeform-txt: #A6DAE3;
  --border-width: 1px;
}

li.blurb h4.heading a[rel="author"] {
  font-size: 0.85em !important;
  font-weight: 400 !important;
  color: #aca7c6 !important;
}

li.blurb h4.heading a[href*="/works/"],
li.blurb h4.heading a {
  font-size: 1.3em !important;
  font-weight: bold !important;
}

h2.title.heading {
  color: #ef6d93 !important;
  font-size: 2.0em !important;
  font-weight: bold !important;
}

a.tag:not(.fandom.index.group a.tag):not(h2.heading a.tag):not(.splash .favorite a.tag):not(.splash .favorite li:nth-of-type(2n+1) a.tag),
.tags a[data-remote="true"],
.unwrangled,
.added.tag {
  background-color: transparent !important;
  color: var(--tag-freeform-txt);
  border: var(--border-width) solid var(--tag-freeform-txt);
}

a.tag:not(.fandom.index.group a.tag,
h2.heading a.tag,
.splash .favorite a.tag):is(:hover,
:focus),
.listbox .heading a.tag:visited:is(:hover,
:focus),
.tags a[data-remote="true"]:is(:hover,
:focus) {
  border: 1px solid var(--txt-alt1) !important;
  transition: 0.2s ease;
}

.blurb h5.fandoms.heading,
dd.fandom.tags {
  display: block;
  margin-top: 0 !important;
  margin-bottom: 0 !important;
  line-height: 1.2em !important;
  position: relative;
}

li.blurb h5.fandoms.heading a.tag:nth-child(n+3),
li.blurb dd.fandom.tags a:nth-child(n+3) {
  display: none !important;
}

li.blurb h5.fandoms.heading:hover a.tag,
li.blurb dd.fandom.tags:hover a {
  display: inline-block !important;
}

li.blurb h5.fandoms.heading a.tag:nth-last-child(n+2)::after,
li.blurb dd.fandom.tags a:nth-last-child(n+2)::after {
  content: "✴";
  font-size: 1.1em !important;
  font-weight: normal !important;
  color: #ffe4c4 !important;
  display: inline-block !important;
  margin-left: 0.25em !important;
  cursor: default;
}

li.blurb h5.fandoms.heading:hover a.tag::after,
li.blurb dd.fandom.tags:hover a::after {
  display: none;
}

.blurb h5.fandoms.heading a.tag,
dd.fandom.tags a {
  border: none !important;
  background: none !important;
  padding: 0.15em 0.15em !important;
  margin: 0 0.1em 0 0 !important;
  display: inline-block;
  font-weight: 700 !important;
  color: var(--tag-fandom-txt) !important;
  font-size: 1.2em !important;
  line-height: 1.2em !important;
  vertical-align: top;
}

li.warnings a.tag,
dd.warning.tags a {
  border: none !important;
  background: none !important;
  padding: 0 !important;
  text-decoration: none !important;
  font-weight: 380 !important;
  color: var(--tag-warning-txt) !important;
}

[class^="relationship"] a.tag {
  border: 1px solid var(--tag-ship-txt) !important;
}

li.relationships:has(a[href*="%20*a*%20"]) a.tag,
[class^="relationship"] a[href*="%20*a*%20"],
[class^="relationship"] a[href^="/tags/Other%20Relationship%20Tags%20to%20Be%20Added"] {
  border: 1px solid var(--tag-platonic-ship-txt) !important;
  color: var(--tag-platonic-ship-txt) !important;
}

[class^="character"] a.tag {
  border: 1px solid var(--tag-character-txt) !important;
}

[class^="freeform"] a.tag {
  border: 1px solid var(--tag-freeform-txt) !important;
}

.unwrangled {
  border: var(--border-width) dashed var(--tag-freeform-txt) !important;
  background: transparent;
}

.autocomplete li.added,
.post .meta dd ul li.added {
  padding: 2px 8px;
  color: var(--tag-freeform-txt);
  border: var(--border-width) solid var(--tag-freeform-txt);
}

li.added:is(:hover,
:focus) {
  border-color: var(--txt-alt2);
  color: var(--txt-alt2);
}

li.added:is(:hover,
:focus) .delete a {
  color: inherit;
}

.delete a,
span.delete,
span.delete a {
  color: var(--tag-freeform-txt);
}

.delete a:hover,
span.delete:hover,
span.delete a:hover {
  color: var(--txt-alt2) !important;
}

body .blurb ul.fandom.tags,
body .blurb h5.fandoms.heading,
body dd.fandom.tags {
  display: block !important;
  width: 100% !important;
  clear: both !important;
  float: none !important;
  margin-top: 0.35em !important;
}

body .blurb .header,
body .blurb .datetime {
  display: inline-block !important;
  vertical-align: middle !important;
}

body .blurb .datetime {
  float: right !important;
  margin-left: 1em !important;
}

body .blurb ul.fandom.tags[style*="display: none"],
body .blurb ul.fandom.tags.hidden {
  display: block !important;
  float: none !important;
  clear: both !important;
  width: 100% !important;
}

li.relationships a.tag,
dd.relationship.tags a.tag,
li.characters a.tag,
body .blurb .characters a.tag,
li.freeforms a.tag,
body .blurb .freeforms a.tag {
  font-size: 1.0em !important;
}

body [class^="warning"] a.tag span.text {
  display: none !important;
}

body [class^="warning"] a.tag::after {
  display: inline-block !important;
  margin-left: 0.3em !important;
  font-weight: 700 !important;
  font-size: 0.85em !important;
  line-height: 1 !important;
  color: var(--tag-warning-txt) !important;
  padding: 0.05em 0.35em !important;
}

body [class^="warning"] a.tag[href*="Graphic%20Depictions%20Of%20Violence"]::after {
  content: "⛓⚑" !important;
}


body [class^="warning"] a.tag[href*="Underage%20Sex"]::after {
  content: "U-Sex" !important;
}

body [class^="warning"] a.tag[href*="No%20Archive%20Warnings%20Apply"]::after {
  content: "◌" !important;
}

body [class^="warning"] a.tag[href*="Creator%20Chose%20Not%20To%20Use%20Archive%20Warnings"]::after {
  content: "✒" !important;
}

body li.warnings {
  display: block !important;
  width: 100% !important;
  clear: both !important;
  float: none !important;
  margin: 0.2em 0 0.1em 0 !important;
  padding: 0 !important;
}

body li.warnings a.tag {
  padding: 0.05em 0.35em !important;
  font-size: 0.85em !important;
  line-height: 1.1 !important;
  font-weight: 450 !important;
}

/* ==========================================
   Nome file: Rosé Pine - Tablet.ketty.css
   Autore originale: BlackBatCat
   Tipo: Skin AO3
   Descrizione: Ottimizzazione della skin Rosé Pine per tablet. 
                Necessaria per poter usare la versione Mobile.ketty.
                
   Important: The tablet and mobile skins are not optional and must be included for the theme to work properly.
   Under Advanced → Choose @media, select: only screen (max-width: 62em).
   ========================================== */

#inner {
  flex-flow: column;
}

#header .heading {
  margin-left: var(--margins-narrow);
}

#login,
#greeting {
  margin-right: var(--margins-narrow);
}

#header .primary {
  justify-content: center;
}

#header h2 {
  text-align: center;
}

#dashboard,
#dashboard.own {
  top: unset;
  z-index: 2;
  width: auto;
  min-width: unset;
  max-width: unset;
  height: auto;
  max-height: unset;
  overflow: visible;
  margin: 2% 2% 0 2%;
  padding: 0;
  border-bottom: var(--border-width) solid;
  text-align: center;
}

#dashboard ul {
  box-sizing: border-box;
  width: 100%;
  margin: 0;
  padding: 0.25em 0;
  text-align: center;
}

#dashboard a,
#dashboard span {
  display: inline-block;
  margin-block: var(--border-width);
}

#dashboard .secondary {
  position: absolute;
  left: 50%;
  width: fit-content;
  max-width: 95%;
  transform: translate(-50%, 0);
}

#main,
#main.dashboard {
  width: 100%;
  padding-inline: var(--margins-narrow);
}

.logged-in .splash>.module {
  width: 48.5%;
}

.region:has(ol.pagination.actions) form.filters {
  margin-bottom: 7.5em !important;
}

/* ==========================================
   Nome file: Rosé Pine - Mobile.ketty.css
   Autore originale: BlackBatCat
   Tipo: Skin AO3
   Descrizione: Ottimizzazione della skin Rosé Pine per mobile. 
                Necessaria la presenza della versione Tablet.ketty.

   Important: The tablet and mobile skins are not optional and must be included for the theme to work properly.
   Under Advanced → Choose @media, select: only screen (max-width: 42em).
   ========================================== */

h2.heading,
h2.heading+h3.heading:not(.landmark) {
  display: inline-block;
  width: 100%;
  margin-top: 0;
  text-align: center;
}

#header .heading a::before {
  content: "AO3\00a0✿";
}

#header .menu {
  width: 96%;
  max-width: unset;
  min-width: unset;
  border-inline: none;
  border: var(--border-width) solid var(--border1);
  transform: unset;
  margin: 0 2%;
}

#header .menu li {
  text-align: center;
}

#login,
#greeting {
  order: 2;
}

#header nav:has(> .primary) {
  min-width: 100%;
  max-width: 100%;
  border-top: var(--border-width) solid;
}

#header li.search {
  position: absolute;
  top: 0.7em;
}

#header #search .text {
  width: 35vw;
  min-width: unset;
  max-width: unset;
  transition: width 0.15s;
}

#header #search .text:is(:focus,
:active) {
  width: 95vw;
  max-width: unset;
}

#dashboard,
#dashboard.own {
  top: unset;
  z-index: 2;
  width: auto;
  min-width: unset;
  max-width: unset;
  height: auto;
  max-height: unset;
  overflow: visible;
  margin: 2% 2% 0 2%;
  padding: 0;
  border-bottom: var(--border-width) solid;
  text-align: center;
}

#dashboard ul {
  box-sizing: border-box;
  width: 100%;
  margin: 0;
  padding: 0.25em 0;
  text-align: center;
}

#dashboard a,
#dashboard span {
  display: inline-block;
  margin-block: var(--border-width);
}

#dashboard .secondary {
  position: absolute;
  left: 50%;
  width: fit-content;
  max-width: 95%;
  transform: translate(-50%, 0);
}

.filtered .index,
form.filters,
form dd,
form dt,
form .meta dd,
form .meta dt,
form.inbox {
  float: none;
  width: 100%;
  min-width: 0;
  max-width: 100%;
}

#footer {
  padding-block: 5%;
}

#footer ul.navigation.actions {
  flex-wrap: wrap;
}

#footer ul li.module {
  flex-basis: 47.5%;
}

#footer ul li.module:nth-of-type(-n+2) {
  margin-bottom: 5%;
}

ul.navigation.actions,
p.navigation.actions {
  float: none;
  display: block;
  text-align: center;
}

.module h3.landmark {
  display: none;
}

.javascript .work.navigation .download .secondary {
  flex-direction: column;
}

.icon {
  width: 85px;
  height: 85px;
}

.tagset .media .listbox {
  width: 100%;
  margin-right: 0;
}

.bookmark .short .header {
  align-items: flex-start;
}

.home .header h2,
.home .header ul.actions {
  margin-left: 0;
  border-bottom: 0;
  text-align: center;
}

.home .header h2 {
  order: 2;
  margin-block: 0.429em;
}

.primary .icon {
  order: 1;
  position: unset;
  margin: 0 auto;
}

.home .header ul.actions,
.home .navigation.actions {
  order: 3;
}

.home .header .userstuff {
  order: 4;
}

.home .header .type {
  order: 5;
  width: 100%;
  text-align: center;
}

.home .header dl.stats {
  order: 6;
}

.javascript form.filters {
  overflow-y: visible;
  max-height: unset;
  padding: 0 0.643em;
}

.region:has(ol.pagination.actions) form.filters {
  background-color: var(--bg5);
  border: var(--border-width) solid var(--border1);
  box-shadow: var(--shadow-header);
}

.javascript {
  background: var(--bg1);
}

.media-index .media .listbox {
  width: 100%;
}

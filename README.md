# shellya-site.github.io
# hello, world!

<html>
<head>
<style>
/* Basic CSS for tabs */
.tab {
  overflow: hidden;
  border: 1px solid #ccc;
  background-color: #f1f1f1;
}

.tab button {
  background-color: inherit;
  float: left;
  border: none;
  outline: none;
  cursor: pointer;
  padding: 14px 16px;
  transition: 0.3s;
}

.tab button:hover {
  background-color: #ddd;
}

.tabcontent {
  display: none;
  padding: 6px 12px;
  border: 1px solid #ccc;
  border-top: none;
}
</style>
</head>
<body>

<div class="tab">
  <button class="tablinks" onclick="openTab(event, 'Tab1')">Tab 1</button>
  <button class="tablinks" onclick="openTab(event, 'Tab2')">Tab 2</button>
  <button class="tablinks" onclick="openTab(event, 'Tab3')">Tab 3</button>
</div>

<div id="Tab1" class="tabcontent">
  <h3>Tab 1 Content</h3>
  <p>This is the content for Tab 1.</p>
</div>

<div id="Tab2" class="tabcontent">
  <h3>Tab 2 Content</h3>
  <p>This is the content for Tab 2.</p>
</div>

<div id="Tab3" class="tabcontent">
  <h3>Tab 3 Content</h3>
  <p>This is the content for Tab 3.</p>
</div>

<script>
function openTab(evt, tabName) {
  var i, tabcontent, tablinks;
  tabcontent = document.getElementsByClassName("tabcontent");
  for (i = 0; i < tabcontent.length; i++) {
    tabcontent[i].style.display = "none";
  }
  tablinks = document.getElementsByClassName("tablinks");
  for (i = 0; i < tablinks.length; i++) {
    tablinks[i].className = tablinks[i].className.replace(" active", "");
  }
  document.getElementById(tabName).style.display = "block";
  evt.currentTarget.className += " active";
}
//sets the first tab to be open by default.
document.getElementsByClassName("tablinks")[0].click()
</script>

</body>
</html>


<html>
<head>
<style>
body {
  display: flex; /* Use flexbox for layout */
}

.side-tabs {
  width: 200px;
  background-color: #f0f0f0;
  padding: 10px;
  display: flex;
  flex-direction: column; /* Stack tabs vertically */
}

.side-tabs button {
  padding: 10px;
  margin-bottom: 5px;
  border: none;
  background-color: #ddd;
  cursor: pointer;
}

.side-tabs button.active {
  background-color: #bbb;
}

.content-area {
  flex-grow: 1; /* Allow content area to expand */
  padding: 20px;
}

.tab-content {
  display: none;
}

.tab-content.active {
  display: block;
}
</style>
</head>
<body>

<div class="side-tabs">
  <button onclick="showTab('tab1')" class="active">Tab 1</button>
  <button onclick="showTab('tab2')">Tab 2</button>
  <button onclick="showTab('tab3')">Tab 3</button>
</div>

<div class="content-area">
  <div id="tab1" class="tab-content active">
    <h3>Tab 1 Content</h3>
    <p>This is the content for Tab 1.</p>
  </div>
  <div id="tab2" class="tab-content">
    <h3>Tab 2 Content</h3>
    <p>This is the content for Tab 2.</p>
  </div>
    <div id="tab3" class="tab-content">
    <h3>Tab 3 Content</h3>
    <p>This is the content for Tab 3.</p>
  </div>
</div>

<script>
function showTab(tabId) {
  const tabContents = document.querySelectorAll('.tab-content');
  tabContents.forEach(content => content.classList.remove('active'));

  const tabs = document.querySelectorAll('.side-tabs button');
  tabs.forEach(tab => tab.classList.remove('active'));

  document.getElementById(tabId).classList.add('active');
  event.target.classList.add('active');
}
</script>

</body>
</html>

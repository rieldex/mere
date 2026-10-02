---
layout: wiki
title: Main Page
---

<!-- TW/CW Modal -->
<div id="twcw-modal">
  <div class="twcw-backdrop">
    <div class="twcw-content">
      <h2>Content Warning</h2>
      <p>This wiki contains depictions of:</p>
      <ul>
        <li>Graphic violence and torture</li>
        <li>Psychological abuse and manipulation</li>
        <li>Death, necromancy, and body horror</li>
        <li>Suicide and self-harm</li>
        <li>Non-consensual magical compulsion / mind control</li>
        <li>Child abuse (medical experimentation)</li>
      </ul>
      <p>Additional themes include obsessive/codependent relationships, identity erasure, and grief/madness.</p>
      
      <div class="twcw-actions">
        <button onclick="dismissTWCW()" class="twcw-btn">Enter Wiki</button>
        <button onclick="goBack()" class="twcw-btn secondary">Go Back</button>
      </div>
      <p class="twcw-note">This warning will not appear again on this device.</p>
    </div>
  </div>
</div>

<!-- Your actual homepage content starts here -->
<div id="main-content" style="display:none;">

<h2 class="acc">Welcome to The Annals of the Thorned Mere</h2>

<p>A comprehensive record of the Kingdoms of Thornmere, Vet Engi, and the Eastern Marches. 
This encyclopedia documents the history, politics, and personages of a world divided between 
three powers, where magic flows through bloodlines and ancient faiths shape the destiny of nations.</p>

<h3 class="acc2">Quick Navigation</h3>
<ul>
  <li><strong>Regions:</strong> Explore <a href="{{ '/regions/thornmere' | relative_url }}">Thornmere</a>, <a href="{{ '/regions/vetengi' | relative_url }}">Vet Engi</a>, and the <a href="{{ '/regions/east' | relative_url }}">Eastern Marches</a></li>
  <li><strong>Characters:</strong> Browse <a href="{{ '/chars/main' | relative_url }}">main characters</a>, <a href="{{ '/chars/historical' | relative_url }}">historical figures</a>, and <a href="{{ '/chars/world' | relative_url }}">world characters</a></li>
  <li><strong>History:</strong> View the <a href="{{ '/history/timeline' | relative_url }}">modern timeline</a> or <a href="{{ '/history/historical' | relative_url }}">historical records</a></li>
  <li><strong>Faith:</strong> Learn about <a href="{{ '/faith/tetratism' | relative_url }}">Tetratism</a> and the <a href="{{ '/faith/twelve' | relative_url }}">Faith of the Twelve</a></li>
</ul>

<h3 class="acc2">Setting Overview</h3>
<p><strong>Themes:</strong> Gothic Horror | Medieval Fantasy | Medium Magic<br>
<strong>Current Year:</strong> 1527<br>
<strong>Magic System:</strong> Innate gift tied to spirit resonance, with blood magic as the ultimate taboo.</p>

</div>

<script>
function dismissTWCW() {
  localStorage.setItem('twcw-acknowledged', 'true');
  document.getElementById('twcw-modal').style.display = 'none';
  document.getElementById('main-content').style.display = 'block';
  document.body.classList.remove('modal-open');
}

function goBack() {
  history.back();
}

// Check on load
if (!localStorage.getItem('twcw-acknowledged')) {
  document.getElementById('twcw-modal').style.display = 'block';
  document.body.classList.add('modal-open');
} else {
  document.getElementById('main-content').style.display = 'block';
}
</script>

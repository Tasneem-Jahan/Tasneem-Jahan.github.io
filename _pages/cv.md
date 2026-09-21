---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<div class="cv-action-bar">
  <a href="{{ '/files/CV_Tasneem_Jahan_Farheen.pdf' | relative_url }}" class="btn btn--primary" target="_blank">
    <i class="fas fa-file-pdf"></i> Download Full CV (PDF)
  </a>
  <a href="https://github.com/Tasneem-Jahan" class="btn btn--outline" target="_blank">
    <i class="fab fa-github"></i> GitHub Profile
  </a>
</div>

<!-- Embedded Scrollable PDF Viewer -->
<div class="pdf-viewer-container">
  <object
    data="{{ '/files/CV_Tasneem_Jahan_Farheen.pdf' | relative_url }}"
    type="application/pdf"
    width="100%"
    height="1000px"
  >
    <!-- Fallback if browser/device cannot render embedded PDF -->
    <div class="pdf-fallback">
      <p>Your browser does not support embedded PDF viewing.</p>
      <a href="{{ '/files/CV_Tasneem_Jahan_Farheen.pdf' | relative_url }}" class="btn btn--primary" target="_blank">
        <i class="fas fa-file-pdf"></i> Click here to view and download the CV
      </a>
    </div>
  </object>
</div>

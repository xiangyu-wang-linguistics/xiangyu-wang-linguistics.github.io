---
layout: single
title: "CV"
permalink: /cv/
description: "Curriculum vitae of Xiangyu Wang, a linguist at the University of Oxford working on syntax, semantics, language acquisition, and computational linguistics."
author_profile: true
redirect_from:
  - /resume
---

{% assign cv_pdf = '/files/cv.pdf' | relative_url %}

My current curriculum vitae is available below.

<div class="cv-pdf__actions">
  <a class="btn btn--info" href="{{ cv_pdf }}" target="_blank" rel="noopener noreferrer">
    <i class="fas fa-file-pdf" aria-hidden="true"></i>
    Open PDF
  </a>
  <a class="btn" href="{{ cv_pdf }}" download>
    <i class="fas fa-download" aria-hidden="true"></i>
    Download PDF
  </a>
</div>

<object class="cv-pdf__viewer" data="{{ cv_pdf }}#view=FitH" type="application/pdf" title="Curriculum vitae of Xiangyu Wang" aria-label="Curriculum vitae of Xiangyu Wang">
  <p class="notice--info">
    Your browser cannot display the PDF preview. <a href="{{ cv_pdf }}" target="_blank" rel="noopener noreferrer">Open the CV as a PDF</a>.
  </p>
</object>

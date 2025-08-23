---
title: Canvas
description: A guide to help students enroll in the Canvas course ELEC0001
author: Kik
---
<div id="loader-wrapper">
    <div class="loader-container">
        <div class="spinner"></div>
        <div class="logo-container">
            <img src="images/makerspace_logo.png" width="80" height="80" alt="Logo">
        </div>
    </div>
</div>

<style>
#loader-wrapper {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: #222222;
    z-index: 9999;
    display: flex;
    justify-content: center;
    align-items: center;
}
.loader-container {
    position: relative;
    width: 120px;
    height: 120px;
    display: flex;
    justify-content: center;
    align-items: center;
}
.spinner {
    position: absolute;
    width: 120px;
    height: 120px;
    border: 4px solid rgba(247, 116, 49, 0.2);
    border-top: 4px solid rgba(247, 116, 49, 1);
    border-radius: 50%;
    animation: spin 1s linear infinite;
}
.logo-container {
    position: absolute;
    width: 80px;
    height: 80px;
    display: flex;
    justify-content: center;
    align-items: center;
}
@keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}
.loader-hidden {
    opacity: 0;
    visibility: hidden;
    transition: visibility 0s 0.3s, opacity 0.3s linear;
}
</style>

<script>
window.addEventListener('load', function() {
    const loader = document.getElementById('loader-wrapper');
    loader.classList.add('loader-hidden');
    loader.addEventListener('transitionend', function() {
        document.body.removeChild(loader);
    });
});

// Show loader during navigation
document.addEventListener('DOMContentLoaded', function() {
    document.querySelectorAll('a').forEach(link => {
        link.addEventListener('click', function() {
            const loader = document.getElementById('loader-wrapper');
            if (loader) {
                loader.classList.remove('loader-hidden');
            }
        });
    });
});
</script>
## Canvas Enrollment Guide

Thank you for applying for a makerspace membership, we are so excited to have you join us. In order to get started, you will need to enroll in the Canvas course ELEC0001, so that you can access our labs and equipment. This guide will walk you through the process of enrolling in the course.

## Who is this guide for?
This guide is for students who have already applied for a makerspace membership and have recieved a confirmation email from us, however get **QUIZ LOCKED** when attempting to complete the quiz.


### Step 0:
Maker sure you already recieved a confirmation email of us receiving your application. It may look like this:
![Confirmation Email](images/email_confirmation.png)

### Step 1:
Click on the canvas link, once on the page click on the top right corner on the "Enroll in Course" button.

It may look like this:
![Canvas Enrollment](images/canvas_enrollement.png)


**Congratulations, you have enrolled in the course**

if you still have any issues, even after following this guide, please contact us at 
ecemakers(at)ust(dot)hk

_this guide was written on 4th Feb_
_by Kik_
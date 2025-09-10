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
<div class="center-content">
    <img src="images/makerspace_logo.png" 
    width="200" height="200"
    alt="MakerSpace Logo" class="center-logo">
    <h1 class="title">ECE MakerSpace Docs</h1>
    <p class="subtitle"><i>For all things makerspace</i></p>
    <p class="subtitle"><a href="https://maker.ece.hkust.edu.hk">Main Website</a></p>
</div>

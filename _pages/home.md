---
title: "Logos Robotics Lab @ ASU - Home"
layout: homelay
excerpt: "Logos Robot Lab @ ASU."
sitemap: false
permalink: /
---

**News: [StageCraft](https://arxiv.org/abs/2603.20659) has been accepted into IROS 2026, where we are also organizing a [workshop on compositional and modular learning](https://compositional-robotics.github.io/)!** 


<div markdown="0" id="carousel" class="carousel slide" data-ride="carousel" data-interval="5000" data-pause="hover" >
    <!-- Menu -->
    <ol class="carousel-indicators">
        <li data-target="#carousel" data-slide-to="0" class="active"></li>
        <li data-target="#carousel" data-slide-to="1"></li>
        <li data-target="#carousel" data-slide-to="2"></li>
        <li data-target="#carousel" data-slide-to="3"></li>
        <li data-target="#carousel" data-slide-to="4"></li>
        <li data-target="#carousel" data-slide-to="5"></li>
    </ol>
    <div class="carousel-inner" markdown="0">
        <div class="item active" data-interval="5000">
            <img src="{{ site.url }}{{ site.baseurl }}/images/slider7001400/IMG_20230713_162520.jpg" alt="Slide2" />
        </div>
        <!-- Each video slide holds for its own clip length; see data-interval. -->
        <div class="item" data-interval="18500">
            <video class="carousel-video" muted playsinline preload="metadata">
                <source src="{{ site.url }}{{ site.baseurl }}/videos/stagecraft_pi05.mp4" type="video/mp4" />
            </video>
        </div>
        <div class="item" data-interval="12000">
            <video class="carousel-video" muted playsinline preload="metadata">
                <source src="{{ site.url }}{{ site.baseurl }}/videos/stagecraft_real.mp4" type="video/mp4" />
            </video>
        </div>
        <div class="item" data-interval="17500">
            <video class="carousel-video" muted playsinline preload="metadata">
                <source src="{{ site.url }}{{ site.baseurl }}/videos/sawyer_14.mp4" type="video/mp4" />
            </video>
        </div>
        <div class="item" data-interval="13500">
            <video class="carousel-video" muted playsinline preload="metadata">
                <source src="{{ site.url }}{{ site.baseurl }}/videos/sawyer_23.mp4" type="video/mp4" />
            </video>
        </div>
        <div class="item" data-interval="6500">
            <video class="carousel-video" muted playsinline preload="metadata">
                <source src="{{ site.url }}{{ site.baseurl }}/videos/fdp_distractor.mp4" type="video/mp4" />
            </video>
        </div>
    </div>
  <a class="left carousel-control" href="#carousel" role="button" data-slide="prev">
    <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="right carousel-control" href="#carousel" role="button" data-slide="next">
    <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div>

<style>
/* Slides carry different aspect ratios (4:3 photos, 16:9 video), so every slide is
   pinned to one 16:9 box to stop the carousel resizing as it advances. Media is
   letterboxed rather than cropped, so nothing gets cut out of the group photos. */
.carousel-inner > .item {
    aspect-ratio: 16 / 9;
    background-color: #000;
}
.carousel-inner > .item > img,
.carousel-inner > .item > .carousel-video {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: contain;
    line-height: 1;
}
</style>

<script>
// Deferred to window load: jQuery and bootstrap.js are pulled in by the footer,
// which is further down the page than this script.
window.addEventListener('load', function () {
    // Videos are only played once their slide is showing, and restarted from the top,
    // so a clip is never caught mid-way through.
    var $carousel = jQuery('#carousel');
    function playActive() {
        $carousel.find('video').each(function () { this.pause(); this.currentTime = 0; });
        var video = $carousel.find('.item.active video')[0];
        if (video) { video.play(); }
    }
    $carousel.on('slid.bs.carousel', playActive);
    playActive();
});
</script>


Welcome to the Logos Robotics Lab. We are a robotics research group based within the [School of Augmented Intelligence](https://scai.engineering.asu.edu/) at [Arizona State University](https://www.asu.edu/). Our aim is to make robots adept at collaborating with people while augmenting human capabilities. 
We achieve these goals by making robots autonomous, collaborative and interactive by solving fundamental problems in Robot Learning, Language Grounding, Task and Motion Planning and Perception.      

 **We are always looking for passionate Undergraduate and Master students to join the team. If you an ASU student please contact Nakul Gopalan for more details.** 

<!-- We are a dynamic research group, at the [Leiden Institute of Physics](http://www.physics.leidenuniv.nl) and soon at [LMU](https://www.physik.lmu.de/en/index.html). Our aim is to explore and understand quantum materials, including strange metals, high-temperature superconductors, and quantum critical electron matter. To this end, we develop new quantum sensing and quantum imaging instrumentation to get the key quantum mechanical degrees of freedom. We want to be able to build the perfect instruments to answer the scientific questions we deem most important (see [Research](research)). 


We are very much looking forward to being part of [LMU physics](https://www.physik.lmu.de/en/index.html)! We will build up our instruments right in the center of the city, in the “Sommerfeldkeller”, where Sommerfeld himself worked. We will exchange ideas with world class groups working in quantum physics, cold-atom many-body physics, and 2d quantum materials.

Our move to LMU will likely start around Summer 2024, depending on the state of renovations. 

Currently, we are located at Leiden University, the birthplace of superconductivity and home to Kamerlingh Onnes, Lorentz, Huygens, Einstein, de Sitter, and others (see e.g. [the wall of signatures from Ehrenfest lecturers](https://www.lorentz.leidenuniv.nl/history/colloquium/muur_heel.html)). 

We are grateful for funding from Leiden University, [LMU ](https://www.lmu.de) [NWO](www.nwo.nl) ([Vidi talent scheme](http://www.nwo.nl/en/research-and-results/programmes/Talent+Scheme) and the [Frontiers in Nanoscience program](https://www.universiteitleiden.nl/en/research/research-projects/science/frontiers-of-nanoscience-nanofront)), and from an [ERC starting and consolidator grants](https://erc.europa.eu/funding/starting-grants). -->

 <!-- **We are  looking for passionate new PhD students, Postdocs, and Master students to join the team** [(more info)]({{ site.url }}{{ site.baseurl }}/vacancies) **!** -->

<div markdown="0" class="connect">
  <span class="connect-label">Connect with us</span>
  <a class="connect-link connect-linkedin" href="https://www.linkedin.com/company/logos-robotics-lab/" target="_blank" rel="noopener">
    <svg xmlns="http://www.w3.org/2000/svg" width="15" height="15" fill="currentColor" viewBox="0 0 16 16" aria-hidden="true">
      <path d="M0 1.146C0 .513.526 0 1.175 0h13.65C15.474 0 16 .513 16 1.146v13.708c0 .633-.526 1.146-1.175 1.146H1.175C.526 16 0 15.487 0 14.854V1.146zm4.943 12.248V6.169H2.542v7.225h2.401zm-1.2-8.212c.837 0 1.358-.554 1.358-1.248-.015-.709-.52-1.248-1.342-1.248-.822 0-1.359.54-1.359 1.248 0 .694.521 1.248 1.327 1.248h.016zm4.908 8.212V9.359c0-.216.016-.432.08-.586.173-.431.568-.878 1.232-.878.869 0 1.216.662 1.216 1.634v3.865h2.401V9.25c0-2.22-1.184-3.252-2.764-3.252-1.274 0-1.845.7-2.165 1.193v.025h-.016l.016-.025V6.169h-2.4c.03.678 0 7.225 0 7.225h2.4z"/>
    </svg>
    LinkedIn
  </a>
  <a class="connect-link connect-x" href="https://x.com/logosrobotics" target="_blank" rel="noopener">
    <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" fill="currentColor" viewBox="0 0 16 16" aria-hidden="true">
      <path d="M12.6.75h2.454l-5.36 6.142L16 15.25h-4.937l-3.867-5.07-4.425 5.07H.316l5.733-6.57L0 .75h5.063l3.495 4.633L12.601.75zm-.86 13.028h1.36L4.323 2.145H2.865l8.875 11.633z"/>
    </svg>
    X
  </a>
</div>

<style>
.connect {
    display: flex;
    align-items: center;
    flex-wrap: wrap;
    gap: 10px;
    margin: 30px 0 10px;
    padding-top: 18px;
    border-top: 1px solid #e5e5e5;
}
.connect-label {
    margin-right: 4px;
    color: #777;
    font-size: 14px;
}
.connect-link {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 5px 12px;
    border: 1px solid #ddd;
    border-radius: 3px;
    color: #555;
    font-size: 14px;
    line-height: 1.4;
    text-decoration: none;
    transition: color .15s ease, border-color .15s ease, background-color .15s ease;
}
.connect-link:hover,
.connect-link:focus {
    color: #fff;
    text-decoration: none;
}
.connect-linkedin:hover,
.connect-linkedin:focus { background-color: #0a66c2; border-color: #0a66c2; }
.connect-x:hover,
.connect-x:focus { background-color: #000; border-color: #000; }
</style>




<!-- <figure class="fourth">
  <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/Logo_Leiden.jpg" style="width: 210px">
  <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/Logo_Nanofront.jpg" style="width: 110px">
  <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/Logo_NWO.jpg" style="width: 120px">
  <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/Logo_ERC.jpg" style="width: 110px">
</figure> -->

---
title: "Get ready for Backstage ContribFest at KubeCon!"
url: "https://backstage.io/blog/2025/10/15/backstage-contribfest-kubecon-guide"
date: "Wed, 15 Oct 2025 00:00:00 GMT"
author: ""
feed_url: "https://backstage.io/blog/rss.xml"
---
<p><img alt="Get ready for Backstage ContribFest at KubeCon!" class="img_ev3q" height="945" src="https://backstage.io/assets/images/backstage-contribfest-kubecon-guide-header-fe03d676bef5d0494147e64e4aba5261.png" width="1800" /></p>
<p>Pack your laptop and mark your calendars! Backstage will once again be taking part in the ContribFest track at KubeCon! Join us at KubeCon 2025 North America in Atlanta on Monday, November 13. Feel free to <a class="" href="https://kccncna2025.sched.com/event/27Nl6/contribfest-level-up-your-open-source-journey-hands-on-backstage-contributions-andre-wanlin-patrik-oldsberg-emma-indal-spotify-aramis-sennyey-doordash-kurt-king-procore" rel="noopener noreferrer" target="_blank">bookmark it on your schedule</a>. Then read on to get yourself prepared for the session beforehand to maximize your time working with other contributors and Backstage experts during the session.</p>
<!-- -->
<h2 class="anchor anchorTargetStickyNavbar_Vzrq" id="contrib-what">Contrib-what?<a class="hash-link" href="https://backstage.io/blog/2025/10/15/backstage-contribfest-kubecon-guide#contrib-what" title="Direct link to Contrib-what?">​</a></h2>
<p>Before we dive into preparation for the Backstage ContribFest session we should probably take a detour and answer the question: What the heck is ContribFest?</p>
<p>ContribFest is a track at KubeCon where various CNCF projects will host hands-on sessions working with their respective communities on contributions towards their projects. You don't have to be a past contributor to participate — new community members are encouraged to join!</p>
<p>These sessions are 75 minutes long and take place in a room with roughly a dozen circular tables that seat about eight people making it easy to work and collaborate. They usually lead off with some getting started steps and then give attendees the rest of the time to work on their contributions with the aid of experts from the project.</p>
<h2 class="anchor anchorTargetStickyNavbar_Vzrq" id="what-to-prepare-before-you-get-there">What to prepare before you get there<a class="hash-link" href="https://backstage.io/blog/2025/10/15/backstage-contribfest-kubecon-guide#what-to-prepare-before-you-get-there" title="Direct link to What to prepare before you get there">​</a></h2>
<p>For the Backstage ContribFest session, there are some preparation steps you can complete on your own well before the session. Let's cover those now:</p>
<h3 class="anchor anchorTargetStickyNavbar_Vzrq" id="1-fork-the-repos">1. Fork the repos<a class="hash-link" href="https://backstage.io/blog/2025/10/15/backstage-contribfest-kubecon-guide#1-fork-the-repos" title="Direct link to 1. Fork the repos">​</a></h3>
<p>You'll have the option to contribute to the Backstage repo or the Backstage Community Plugins repo. To get those onto your system, you need to follow the GitHub <a class="" href="https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo#forking-a-repository" rel="noopener noreferrer" target="_blank">"Forking a repository"</a> guide and fork these:</p>
<ul>
<li class="">Backstage: <a class="" href="https://github.com/backstage/backstage" rel="noopener noreferrer" target="_blank">https://github.com/backstage/backstage</a></li>
<li class="">Backstage Community Plugins: <a class="" href="https://github.com/backstage/community-plugins" rel="noopener noreferrer" target="_blank">https://github.com/backstage/community-plugins</a></li>
</ul>
<h3 class="anchor anchorTargetStickyNavbar_Vzrq" id="2-update-nodejs-and-yarn">2. Update Node.js and Yarn<a class="hash-link" href="https://backstage.io/blog/2025/10/15/backstage-contribfest-kubecon-guide#2-update-nodejs-and-yarn" title="Direct link to 2. Update Node.js and Yarn">​</a></h3>
<p>Backstage has <a class="" href="https://backstage.io/docs/getting-started/#prerequisites" rel="noopener noreferrer" target="_blank">a few prerequisites</a> that you'll need to have in place before you can run Backstage or the various Backstage Community Plugins. Here's what you need:</p>
<ul>
<li class="">
<p>Backstage uses Node.js — you'll want to install version 22 for the session.</p>
<ul>
<li class="">To make this easier, we recommend you use Node Version Manager nvm, you can <a class="" href="https://github.com/nvm-sh/nvm#install--update-script" rel="noopener noreferrer" target="_blank">follow these instructions to install it</a>.</li>
<li class="">Once you have nvm installed, you can run this command to get Node 22 installed and activated: <code>nvm install 22</code></li>
</ul>
</li>
<li class="">
<p>Yarn is the package manager used by Backstage — you'll want to install it as well.</p>
<ul>
<li class="">Simply run <code>corepack enable</code> to do so.</li>
</ul>
</li>
</ul>
<h3 class="anchor anchorTargetStickyNavbar_Vzrq" id="3-test-your-setups">3. Test your setups<a class="hash-link" href="https://backstage.io/blog/2025/10/15/backstage-contribfest-kubecon-guide#3-test-your-setups" title="Direct link to 3. Test your setups">​</a></h3>
<p>Now let's do a quick test to confirm that everything is working.</p>
<p>First, let's check that you can run the Backstage codebase:</p>
<ol>
<li class="">Navigate to your cloned fork of the Backstage repo</li>
<li class="">From the root, run <code>yarn install</code></li>
<li class="">Then run <code>yarn tsc</code></li>
<li class="">Finally run <code>yarn start</code></li>
<li class="">Backstage will open in a new browser window or tab</li>
</ol>
<p>Now, let's check the Backstage Community Plugins:</p>
<ol>
<li class="">Navigate to your your cloned fork of the Backstage Community Plugins repo</li>
<li class="">This repo is structured in a way where there are many plugins that live in their own dedicated workspace — for this test, we'll use the <code>linguist</code> workspace. From the root, run <code>cd workspaces/linguist</code></li>
<li class="">From here run <code>yarn install</code></li>
<li class="">Then run <code>yarn tsc</code></li>
<li class="">Finally run <code>yarn start</code></li>
<li class="">An example Backstage app will open in a new browser window or tab</li>
</ol>
<h3 class="anchor anchorTargetStickyNavbar_Vzrq" id="bonus-check-out-the-contribution-guides">Bonus: Check out the contribution guides<a class="hash-link" href="https://backstage.io/blog/2025/10/15/backstage-contribfest-kubecon-guide#bonus-check-out-the-contribution-guides" title="Direct link to Bonus: Check out the contribution guides">​</a></h3>
<p>At this point, you have all the prerequisites in place and are ready to take part in the Backstage ContribFest session. From here, we recommend you take some time to read the contributions guides as that will get you more familiar with the overall process. Here they are:</p>
<ul>
<li class=""><a class="" href="https://github.com/backstage/backstage/blob/master/CONTRIBUTING.md" rel="noopener noreferrer" target="_blank">Backstage Contribution Guide</a></li>
<li class=""><a class="" href="https://github.com/backstage/community-plugins/blob/main/CONTRIBUTING.md" rel="noopener noreferrer" target="_blank">Backstage Community Plugins Contribution Guide</a></li>
</ul>
<h2 class="anchor anchorTargetStickyNavbar_Vzrq" id="-see-you-in-atlanta">👋 See you in Atlanta!<a class="hash-link" href="https://backstage.io/blog/2025/10/15/backstage-contribfest-kubecon-guide#-see-you-in-atlanta" title="Direct link to 👋 See you in Atlanta!">​</a></h2>
<p>On behalf of myself and the other co-hosts of Backstage ContribFest, thanks for following along! We look forward to seeing you in Atlanta and working with you on your contributions. Make sure to say hello!</p>

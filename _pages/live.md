---
layout: splash
title: AZUG live
tagline: Event livestream
permalink: /live
---

<script>
	function refreshData() {
		$.ajax({
            url: 'https://balliauw.blob.core.windows.net/public/azug/azug-live.json?salt=' + (new Date()).toString(),
            dataType: 'jsonp'
        });
	}
	
	function updateStream(data) {
		if (data.IsLive) {
			$('#live').show();
			$('#notlive').hide();
			
			if (data.Speaker) {
				$('#speaker').text(data.Speaker);
			}
			
			if (data.Title) {
				$('#title').text(data.Title);
			}
			
			if (data.EmbedId != '') {
				if ($('#livestream').attr('src') != 'http://www.youtube.com/embed/' + data.EmbedId + '?autoplay=1') {
					$('#livestream').attr('src', 'http://www.youtube.com/embed/' + data.EmbedId + '?autoplay=1');
				}
			}
		} else {			
			$('#notlive').show();
			$('#live').hide();
			$('#livestream').attr('src', '');
			
			if (data.MessageTitle != '') {
				$('#notlive').html('<h1>' + data.MessageTitle + '</h1><p>' + data.MessageBody + '</p>').show();
			} else {
				$('#notlive').html('<h1>No livestream is in progress</h1><p>There is currently no livestream in progress. If you want to watch the archive of sessions we have recorded, check <a href="/videos">our videos page</a>.').show();
			}
		}
	}
	
	$(function() {
		refreshData();
		setInterval(function() {
            refreshData();
		}, 10000);
	});
</script>
<div id="live" style="display: none; text-align: center;">
<h1 id="title"></h1><h2 id="speaker"></h2>
<h3>Questions? Comments? Tweet <a href="https://twitter.com/azugbe" target="_blank">@azugbe</a>!</h3>
<iframe id="livestream" width="560" height="315" src="//www.youtube.com/embed/EYswcoCxE1s" frameborder="0" allowfullscreen></iframe>
</div>
<div id="notlive" style="text-align: center;">
<h1>No livestream is in progress</h1>
<p>There is currently no livestream in progress. If you want to watch the archive of sessions we have recorded, check <a href="/videos">our videos page</a>.</p>
</div>

<hr>

<p style="text-align: center;">
<a href="http://www.realdolmen.com"><img alt="" src="/assets/media/sponsors/logo-realdolmen.jpg" vspace="10" /></a>&nbsp;<a href="http://www.cronos.be"><img alt="" src="/assets/media/sponsors/logo-cronos.jpg" vspace="10" /></a>&nbsp;<a href="http://www.microsoft.be"><img alt="" src="/assets/media/sponsors/logo-microsoft.jpg" vspace="10" /></a>&nbsp;<a href="http://www.euri.com"><img alt="" src="/assets/media/sponsors/logo-euricom.jpg" vspace="10" /></a><br /><a href="http://www.codit.be"><img alt="" src="/assets/media/sponsors/logo-codit.jpg" vspace="10" /></a>&nbsp;<a href="http://www.ae.be"><img alt="" src="/assets/media/sponsors/logo-ae.jpg" vspace="10" /></a>&nbsp;<a href="http://www.cnext.eu"><img alt="" src="/assets/media/sponsors/logo-cnext.jpg" vspace="10" /></a>&nbsp;<a href="http://www.barracuda.com"><img alt="" src="/assets/media/sponsors/logo-barracuda.jpg" vspace="10" /><br /></a><a href="http://www.messagehandler.net"><img alt="" src="/assets/media/sponsors/logo-messagehandler.png" vspace="10" /></a>&nbsp;<a href="http://www.tobania.be/"><img alt="" src="/assets/media/sponsors/logo-tobania.jpg" vspace="10" /></a>&nbsp;<a href="http://www.synergics.be"><img alt="" src="/assets/media/sponsors/logo-synergics.jpg" vspace="10" /></a>&nbsp;<a href="https://www.be.capgemini.com/"><img alt="" src="/assets/media/sponsors/logo-capgemini.jpg" vspace="10" /><br /></a><a href="http://www.stylelabs.com/"><img alt="" src="/assets/media/sponsors/logo-stylelabs.jpg" vspace="10" /></a>&nbsp;<a href="http://www.jetbrains.com"><img alt="" src="/assets/media/sponsors/logo-jetbrains.jpg" vspace="10" /></a>&nbsp;<a href="http://www.xylos.be"><img alt="" src="/assets/media/sponsors/logo-xylos.jpg" vspace="10" /></a>
</p>

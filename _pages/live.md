---
layout: splash
title: AZUG live
tagline: Event livestream
permalink: /live
---

<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
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
				if ($('#livestream').attr('src') != 'https://www.youtube.com/embed/' + data.EmbedId + '?autoplay=1') {
					$('#livestream').attr('src', 'https://www.youtube.com/embed/' + data.EmbedId + '?autoplay=1');
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
<iframe id="livestream" width="560" height="315" src="//www.youtube.com/embed/EYswcoCxE1s" frameborder="0" allowfullscreen></iframe>
</div>
<div id="notlive" style="text-align: center;">
<h1>No livestream is in progress</h1>
<p>There is currently no livestream in progress. If you want to watch the archive of sessions we have recorded, check <a href="/videos">our videos page</a>.</p>
</div>

<hr />

<div class="partners-narrow">
	{% include partners.html %}
</div>
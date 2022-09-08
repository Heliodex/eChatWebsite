<svelte:head>
	<title>eChat</title>
</svelte:head>

<div class="grid">
	<div>
		<img class="eccb" src="eccb.webp" alt="eChat on a Chromebook 11 3189" />
	</div>
	<div class="homepageInfoContainer">
		<div class="homepageInfo">
			<img class="mainLogo" src="green.svg" alt="Green eChat logo" />
			<p>
				A simple chat app in a popup.<br />
				Chat in groups, or one on one.<br />
			</p>
		</div>
	</div>
</div>
<div class="thinpage">
	<div class="thintext">
		<h1>How to install</h1>
		<p>eChat was originally planned to be a browser extension, but these are often blocked on enterprise or school devices. Instead, we went with a different approach that allows eChat to be displayed over the top of almost any webpage.</p>
		<br />
		<h4>Step 1</h4>
		<p>Press Ctrl + Shift + B in your browser to make sure that the Bookmarks Bar is visible.</p>
		<br />
		<h4>Step 2</h4>
		<p>Drag this into any free space in your Bookmarks Bar: <a href="javascript:if(document.getElementById('eChatWindow')){'{'}const e=document.getElementById('eChatWindow');Object.assign(e.style,{'{'}display:'block'==getComputedStyle(e).getPropertyValue('display')?'none':'block'})}else{'{'}let e=document.createElement('script');e.src='https://cdn.jsdelivr.net/gh/heliodex/echatpopup/m.js',document.body.appendChild(e)}" id="bookmarklet">eChat</a></p>
		<br />
		<h4>Step 3</h4>
		<p>
			Click on the newly created bookmark. An eChat popup window should appear over the current website!<br />
			You can drag the popup around by the header, close it using the close button, and re-open it by clicking the bookmark again.<br /><br />
			Click the "i" icon in the top-left corner for help with using eChat.
		</p>
		<br /><br />
		<h4 id="issues">Common issues</h4>
		<p>
			<em>- The popup does not appear after clicking the bookmark!</em><br />
			This is likely because of CORS policies set by the owner of the current website, preventing the popup from loading. There's nothing we can do about this, sorry :(. Try using eChat on a different site.<br />
		</p>
		<p>
			<em>- The popup appears after clicking the bookmark, but the eChat window is blank!</em><br />
			This is probably because the site is using an insecure connection to the server. eChat does not operate over insecure connections, as this could allow an attacker to intercept messages. Try using eChat on a different site that shows a padlock icon in the URL bar.<br />
		</p>
		<p>If your issue is not listed here or is still ongoing, please contact our support team at <a href="mailto:help.echat@gmail.com">help.echat@gmail.com</a> so we can resolve the problem.</p>
	</div>
</div>

<style lang="sass">
	#bookmarklet
		color: white
		text-decoration: none
		padding: 1.5%
		margin: 0 0.5rem
		border-radius: 0.5rem
		pointer-events: drag

	.thinpage
		margin-top: 15vh

	h1, #issues
		text-align: center

	h4
		font-size: 1.25rem

	.eccb
		position: absolute
		object-fit: contain
		height: 60vh
		margin-top: 3%
		right: 50%
		max-width: 60vh
		visibility: hidden
	
	.grid
		width: 100%
		display: grid
		grid-template-columns: 1fr 1fr
		column-gap: 0.7rem

	.homepageInfo
		margin-left: 2rem
		display: flex
		flex-direction: column

	.mainLogo
		width: 30vw
		max-width: 20rem
		margin-top: 30vh

	@media screen and (max-width: 599px)

		.grid
			grid-template-columns: 0fr 1fr
			justify-content: center

		.mainLogo
			width: 60vw
			max-width: 28rem

		.homepageInfo
			margin: 0
		.homepageInfoContainer
			display: flex
			justify-content: center

	@media screen and (min-width: 600px)

		.eccb
			visibility: visible
</style>

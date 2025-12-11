<script lang="ts">
	import profileImg from '$lib/assets/profile.png';
</script>

<aside class="left-side">
	<div class="image">
		<img src={profileImg} alt="" />
		<span class="top-right"></span>
		<span class="bottom-left"></span>
	</div>

	<div>
		<p class="key">name</p>
		<p class="value">Wai Yan Htet</p>
	</div>

	<div>
		<p class="key">Occupation</p>
		<p class="value">software developer</p>
	</div>

	<div>
		<p class="key">Corporation</p>
		<p class="value">freelance</p>
	</div>

	<div>
		<p class="key">‌availability</p>
		<p class="value">24 hours</p>
	</div>

	<div>
		<p class="key">socials</p>
		<p class="value">24 hours</p>
	</div>
</aside>

<style>
	.left-side {
		display: flex;
		flex-direction: column;
		gap: 1.5rem;
	}

	.left-side div {
		text-transform: uppercase;
		letter-spacing: 2px;
	}

	.left-side div .key {
		color: white;
		font-family: var(--secondary-font);
	}

	.left-side div .value {
		color: var(--primary);
		font-size: 18px;
		font-weight: bold;
	}

	.image {
		width: 100px;
		height: 100px;
		position: relative;
		padding: 10px;
		border: 1px solid var(--border-gray);
	}

	img {
		display: block;
		width: 100%;
		height: 100%;
		object-fit: cover;
	}

	.image::before,
	.image::after {
		content: '';
		position: absolute;
		width: 7px;
		height: 7px;
		border: 3px solid #ff2a2a;
	}

	.image::before {
		top: -2px;
		left: -2px;
		border-right: none;
		border-bottom: none;
	}

	.image::after {
		bottom: -3px;
		right: -2px;
		border-left: none;
		border-top: none;
	}

	.image span {
		position: absolute;
		width: 7px;
		height: 7px;
		border: 3px solid #ff2a2a;
	}

	.image span.top-right {
		top: -2px;
		right: -2px;
		border-left: none;
		border-bottom: none;
	}

	.image span.bottom-left {
		bottom: -3px;
		left: -2px;
		border-right: none;
		border-top: none;
	}
</style>

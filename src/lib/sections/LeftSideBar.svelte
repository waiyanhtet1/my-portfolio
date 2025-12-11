<script lang="ts">
	import profileImg from '$lib/assets/profile.png';
	import Button from '$lib/components/Button.svelte';
	import { Github, Linkedin } from '@lucide/svelte';
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
		<div class="socials">
			<a href="https://www.linkedin.com/in/wai-yan-htet-43485a176/" target="_blank">
				<Button size="sm">
					<div class="social">
						<p>linkedin</p>
						<Linkedin size={18} />
					</div>
				</Button>
			</a>
		</div>

		<a href="https://github.com/waiyanhtet1" target="_blank">
			<Button size="sm">
				<div class="social">
					<p>github</p>
					<Github size={18} />
				</div>
			</Button>
		</a>
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
		margin-bottom: 3px;
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

	.socials {
		margin: 10px 0;
	}

	.social {
		width: 150px;
		display: flex;
		align-items: center;
		justify-content: space-between;
	}
</style>

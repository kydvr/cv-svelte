<script lang="ts">
	import Section from '$components/Section.svelte';
	import book from 'svelte-awesome/icons/book';
	import briefcase from 'svelte-awesome/icons/briefcase';
	import cogs from 'svelte-awesome/icons/cogs';
	import user from 'svelte-awesome/icons/user';
</script>

<div class="readable-area">
	<a class="header" href="./photo.html">
		<div class="header-text">
			<h1>Taylor Swift</h1>
			<p>Singer-Songwriter</p>
		</div>
		<img
			alt="Taylor Swift"
			class="Singer-Songwriter"
			src="https://www.refinery29.com/images/9929748.jpg"
		/>
	</a>

	<div class="content">
		<Section iconData={user} title="Long Story Short,">
			<p>
				Taylor Swift is a globally renowned singer-songwriter whose music resonates with millions. With her distinctive voice and relatable lyrics, she has become an influential figure in the music industry. Swift's ability to reinvent herself and connect with her fans has solidified her status as a cultural icon. Beyond her musical talent, she is known for her philanthropy and commitment to making a positive impact in the world.
			</p>
		</Section>
		<Section iconData={book} title="Origins">
			<ul>
					Taylor Swift's meteoric rise to success is a testament to her immense talent and unwavering dedication. Hailing from Pennsylvania, Swift discovered her passion for music at an early age and tirelessly pursued her dreams. With a unique blend of country and pop, she captured the hearts of listeners around the world. Swift's success can be attributed to her relatable storytelling, catchy melodies, and an unbreakable connection with her fans. From her breakthrough self-titled debut album to subsequent chart-topping releases, she has consistently proven her ability to evolve and adapt, cementing her status as one of the most influential and successful artists of her generation.
				<li>
				</li>
			</ul>
		</Section>
		<Section iconData={briefcase} title="Work History">
			<ul>
				<li>
					Head Cook (2022 - ongoing)
					<br />
					&emsp; Krusty Krab, Inc.
				</li>
				<li>
					Marketing Associate (2020 - 2022)
					<br />
					&emsp; Chum Bucket Ltd.
				</li>
				<li>
					Jellyfish Catcher (2018 - 2020)
					<br />
					&emsp; Freelance
				</li>
			</ul>
		</Section>
		<Section iconData={cogs} title="Skills">
			<ul>
				<li>
					<span>Jellyfish Hunting</span>
					<div class="gauge">
						<div class="bullet filled-bullet" />
						<div class="bullet filled-bullet" />
						<div class="bullet filled-bullet" />
						<div class="bullet filled-bullet" />
						<div class="bullet filled-bullet" />
					</div>
				</li>
				<li>
					<span>English</span>
					<div class="gauge">
						<div class="bullet filled-bullet" />
						<div class="bullet filled-bullet" />
						<div class="bullet filled-bullet" />
						<div class="bullet filled-bullet" />
						<div class="bullet" />
					</div>
				</li>
				<li>
					<span>Whale Singing</span>
					<div class="gauge">
						<div class="bullet filled-bullet" />
						<div class="bullet filled-bullet" />
						<div class="bullet filled-bullet" />
						<div class="bullet" />
						<div class="bullet" />
					</div>
				</li>
			</ul>
		</Section>
	</div>
</div>

<style>
	h1 {
		font-family: 'peralta';
	}

	ul {
		list-style-type: none;
	}

	li {
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: space-between;
	}

	li span {
		margin-right: 16px;
	}

	.gauge {
		display: flex;
		flex-direction: row;
	}

	.bullet {
		border-radius: 100%;
		width: 16px;
		height: 16px;
		margin: 4px;
		background-color: #fff59d;
	}

	.filled-bullet {
		background-color: #fbc02d;
	}

	.header-text {
		text-align: center;
		flex: 1;
		margin-right: 16px;
	}

	.readable-area {
		display: flex;
		flex-direction: column;
		background-color: #ffffff;
		margin: 0 5%;
		height: 100%;
	}

	.header {
		padding: 16px;
		display: flex;
		flex-direction: column-reverse;
		align-items: center;
		border-bottom: 2px solid black;
		text-decoration: none;
		color: #000000;
	}

	.content {
		display: grid;
		grid-template-columns: repeat(1, minmax(0, 1fr));
		gap: 32px;
		padding: 32px 32px;
	}

	img {
		width: 128px;
		height: 128px;
		border: 4px solid #000000;
		border-radius: 100%;
	}

	@media (min-width: 600px) {
		.header {
			flex-direction: row;
		}

		.header-text {
			text-align: end;
		}

		.content {
			grid-template-columns: repeat(2, minmax(0, 1fr));
		}

		.readable-area {
			margin: 0 10%;
		}
	}

	@media (min-width: 1000px) {
		.readable-area {
			margin: 0 20%;
		}
	}
</style>

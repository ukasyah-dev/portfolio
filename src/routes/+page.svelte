<script>
	import { CalendarIcon, EnvelopeIcon, GithubIcon, LinkedinIcon, MapPinIcon, XIcon } from '$lib';

	const experience = [
		{
			role: 'Full Stack Developer',
			company: {
				name: 'SMARTM2M Co., Ltd',
				location: 'Bandung, Indonesia'
			},
			duration: 'Nov 2022 - Present',
			responsibilities: [
				'Creating and maintaining web applications using React.js, Node.js, and Express.js',
				'Collaborating with cross-functional teams to deliver high-quality software solutions',
				'Implementing responsive design and ensuring cross-browser compatibility',
				'Optimizing application performance and user experience'
			]
		},
		{
			role: 'Full Stack Developer',
			company: {
				name: 'PT. Melayani Cakrawala Nusantara',
				location: 'Yogyakarta, Indonesia'
			},
			duration: 'Sep 2021 - Nov 2022',
			responsibilities: [
				'Creating and maintaining web applications using React.js, Node.js, and Express.js',
				'Collaborating with cross-functional teams to deliver high-quality software solutions',
				'Implementing responsive design and ensuring cross-browser compatibility',
				'Optimizing application performance and user experience'
			]
		}
	];
</script>

<div class="px-5 pt-28 pb-16 flex flex-col items-center justify-center text-center">
	<img src="/ukasyah.jpeg" alt="UKasyah" class="w-36 h-36 rounded-full mb-6" />

	<h1 class="text-3xl md:text-4xl leading-normal md:leading-snug">Hi! I'm Ukasyah</h1>
	<p class="text-lg leading-relaxed md:leading-8 mt-2.5 max-w-md md:max-w-lg text-neutral-600">
		Full Stack Developer with a keen interest in solving real-world problems and building
		high-impact solutions.
	</p>

	<div class="flex items-center gap-6 mt-7 text-neutral-600">
		<a href="mailto:hi@ukasyah.dev">
			<EnvelopeIcon class="w-6 h-6" />
		</a>
		<a href="https://github.com/ukasyah-dev">
			<GithubIcon class="w-6 h-6" />
		</a>
		<a href="https://www.linkedin.com/in/ukasyah-0454b2220/">
			<LinkedinIcon class="w-6 h-6" />
		</a>
		<a href="https://x.com/ukasyah_dev">
			<XIcon class="w-6 h-6" />
		</a>
	</div>
</div>

<div class="w-full h-[1px] bg-neutral-300 max-w-screen-md mx-auto my-14" />

<div class="w-full max-w-screen-lg mx-auto py-7">
	<h2 class="text-3xl text-center">Professional Experience</h2>

	<div class="flex justify-center gap-10 mt-12">
		{#each experience as exp}
			<div class="flex-1 px-6 py-5 rounded-lg overflow-hidden border border-neutral-300">
				<p class="text-lg font-bold">{exp.role}</p>
				<p class="text-neutral-600 mt-1.5">
					{exp.company.name}
				</p>

				<div class="flex gap-5 text-neutral-600 mt-2">
					<div class="flex items-center gap-1.5">
						<MapPinIcon class="w-5 h-5 text-neutral-500" />
						<span class="text-sm">{exp.company.location}</span>
					</div>
					<div class="flex items-center gap-1.5">
						<CalendarIcon class="w-5 h-5 text-neutral-500" />
						<span class="text-sm">{exp.duration}</span>
					</div>
				</div>

				<p class="font-bold mt-7 mb-3.5">Responsibilities:</p>

				<div class="flex flex-col gap-3.5 text-neutral-600 mb-0.5">
					{#each exp.responsibilities as resp}
						<div class="flex gap-3.5">
							<div class="w-2 h-2 mt-2 rounded-full bg-neutral-400 flex-shrink-0" />
							<p>{resp}</p>
						</div>
					{/each}
				</div>
			</div>
		{/each}
	</div>
</div>

<div class="pb-32" />

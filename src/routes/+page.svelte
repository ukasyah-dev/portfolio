<script>
	import {
		CalendarIcon,
		DockerIcon,
		EnvelopeIcon,
		GithubIcon,
		GoIcon,
		GraphQLIcon,
		KubernetesIcon,
		LinkedinIcon,
		MapPinIcon,
		MySQLIcon,
		NestjsIcon,
		NextIcon,
		PostgreSQLIcon,
		ReactIcon,
		XIcon
	} from '$lib';

	const experience = [
		{
			role: 'Full Stack Developer',
			company: {
				name: 'SMARTM2M Co., Ltd',
				location: 'Bandung, Indonesia'
			},
			duration: 'Nov 2022 - Present',
			responsibilities: [
				'Created and maintained backend services using Nest.js and Go.',
				'Assisted DevOps engineers in deploying applications to Kubernetes, ensuring efficient and reliable operations.',
				'Collaborated with frontend developers to enhance UI and UX, improving overall user satisfaction.',
				'Implemented data duplication across multiple microservices to ensure consistency and reliability.',
				'Developed an identity and access management service utilizing RBAC (Role-Based Access Control).',
				'Implemented gRPC as the service communication protocol to enhance performance and interoperability.',
				'Utilized Kafka and RabbitMQ for asynchronous service communication.',
				'Developed and maintained federated GraphQL services for scalable and unified data access across distributed systems.'
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
				'Created and maintained web applications using Next.js, React.js and Go.',
				'Transformed wireframe designs into a fully functional and visually appealing UI dashboard.',
				'Implementing responsive design and ensuring cross-browser compatibility.',
				'Optimizing application performance and user experience.',
				'Integrated backend services with private S3 storage for secure and efficient data management.',
				'Implemented JWT authentication for secure user access and token refreshing.',
				'Setting up and maintaining CI/CD pipelines (GitLab + AWS).',
				'Mentored junior developers, fostering a collaborative and innovative team environment.'
			]
		}
	];

	const skills = [
		{ icon: GoIcon, iconClassName: 'w-7 h-7', name: 'Golang' },
		{ icon: NestjsIcon, name: 'Nest.js' },
		{ icon: NextIcon, name: 'Next.js' },
		{ icon: ReactIcon, iconClassName: 'w-6 h-6', name: 'React.js' },
		{ icon: MySQLIcon, name: 'MySQL' },
		{ icon: PostgreSQLIcon, name: 'PostgreSQL' },
		{ icon: DockerIcon, iconClassName: 'w-6 h-6', name: 'Docker' },
		{ icon: KubernetesIcon, iconClassName: 'w-6 h-6', name: 'Kubernetes' },
		{ icon: GraphQLIcon, name: 'GraphQL' },
		{ icon: GithubIcon, name: 'GitHub' }
	];
</script>

<div class="pt-20 md:pt-28 pb-16 flex flex-col items-center justify-center text-center">
	<img src="/ukasyah.jpeg" alt="UKasyah" class="w-32 h-32 md:w-36 md:h-36 rounded-full mb-6" />

	<h1 class="text-3xl md:text-4xl leading-normal md:leading-snug">Hi! I'm Ukasyah</h1>
	<p
		class="text-base md:text-lg leading-relaxed md:leading-8 mt-2.5 max-w-md md:max-w-lg text-neutral-600"
	>
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

<div class="w-full h-[1px] bg-neutral-200 max-w-screen-md mx-auto my-12 md:my-14" />

<div class="w-full max-w-screen-lg mx-auto py-7">
	<h2 class="text-2xl md:text-3xl text-center leading-normal">Professional Experience</h2>

	<div class="flex flex-col lg:flex-row justify-center gap-10 mt-12">
		{#each experience as exp}
			<div class="flex-1 px-7 py-6 rounded-lg overflow-hidden border border-neutral-200">
				<p class="text-xl font-bold">{exp.role}</p>
				<p class="text-neutral-600 mt-1.5">
					{exp.company.name}
				</p>

				<div class="flex flex-col md:flex-row gap-2.5 md:gap-4 text-neutral-600 mt-2.5">
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

				<div class="flex flex-col gap-3.5 text-neutral-700 mb-0.5">
					{#each exp.responsibilities as resp}
						<div class="flex gap-3.5">
							<div class="w-2 h-2 mt-2 rounded-full bg-neutral-400 flex-shrink-0" />
							<p class="leading-6">{resp}</p>
						</div>
					{/each}
				</div>
			</div>
		{/each}
	</div>
</div>

<div class="w-full h-[1px] bg-neutral-200 max-w-screen-md mx-auto my-12 md:my-14" />

<div class="w-full max-w-screen-lg mx-auto py-7">
	<h2 class="text-2xl md:text-3xl text-center">Technical Skills</h2>

	<div class="flex flex-wrap justify-center gap-6 mt-12">
		{#each skills as skill}
			<div
				class="px-4 h-11 flex items-center gap-2.5 rounded-lg overflow-hidden border border-neutral-200"
			>
				<svelte:component this={skill.icon} class={skill.iconClassName || 'w-5 h-5'} />
				<p class="leading-none">{skill.name}</p>
			</div>
		{/each}
	</div>
</div>

<div class="pb-20" />

<div class="text-neutral-600 text-center py-8 md:py-10">
	<p>&copy; 2024 - Proudly made in Bandung</p>
</div>

<script lang="ts">
	import '@picocss/pico/css/pico.css';
	import { format } from 'date-fns';

	interface Profile {
		title: string;
		body: string;
		date: Date;
		link: string;
	}

	const pptList: Profile[] = [
		{
			title: 'Orientation',
			body: '수업 관련 안내 사항 전달',
			date: new Date('2024-04-08'),
			link: './ppts/1'
		},
		{
			title: '개발 환경 설정법',
			body: 'VSCode와 확장 프로그램 설정 (HTML, CSS, JS, TS 개요)',
			date: new Date('2024-04.09'),
			link: './ppts/2'
		},
		{
			title: 'HTML 문서 기본 구조',
			body: 'HTML 구조를 살펴만 보기',
			date: new Date('2024.04.09'),
			link: './ppts/3'
		},
		{
			title: 'JavaScript 개발 환경 설정',
			body: 'Node.js, nvm, 패키지 관리자 설치법',
			date: new Date('2024-04.15'),
			link: '/ppts/4'
		}
	];
</script>

<div>
	<main class="fluid-width container">
		<hgroup>
			<p class="text-4xl font-bold">PPT List</p>
			<p>수업 PPT 몰아보기</p>
		</hgroup>

		<table>
			<thead>
				<tr>
					<th></th>
					<th>이름</th>
					<th>내용</th>
					<th>업로드 날짜</th>
					<th>링크</th>
				</tr>
			</thead>
			<tbody>
				{#each pptList as ppt, index}
					<tr>
						<td>{index}</td>
						<td>{ppt.title}</td>
						<td>{ppt.body}</td>
						<td>{format(ppt.date, 'yyyy.MM.dd')}</td>
						<td>
							<a href={ppt.link} data-sveltekit-reload>접속하기</a>
						</td>
					</tr>
				{/each}
			</tbody>
		</table>
	</main>
</div>

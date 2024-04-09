<script lang="ts">
	import VSCodeWebPageImage from './files/code.visualstudio.com-webpage.png';
	import VSCodeExtensions from './files/vscode-extension.png';
	import VSCodePrettier from './files/vscode-prettier.png';
	import VSCodePrettierSetup from './files/vscode-prettier-setup.png';
	import VSCodeGitExtensionPack from './files/vscode-git-extension-pack.png';

	import HTMLIcon from './files/icons8-html-144.png';
	import JSIcon from './files/icons8-js-144.png';
	import TSIcon from './files/icons8-typescript-96.png';
	import CSSIcon from './files/icons8-css-144.png';
</script>

<section>
	<h2>👨‍💻 개발 환경 설정</h2>

	<p>VSCode 설치 (w. 확장 프로그램)</p>
</section>

<!-- 개발환경설정 -->
<section>
	<section>
		<h2>VSCode 설치</h2>
		<img src={VSCodeWebPageImage} alt="" />
		<span class="text-4xl"
			><a href="https://code.visualstudio.com/">https://code.visualstudio.com/</a> 접속</span
		>
	</section>

	<section>
		<h2>확장 프로그램 설치</h2>

		<img src={VSCodeExtensions} alt="" />
		<span class="text-4xl">
			<code>Ctrl + Shift + X</code> 단축키로 확장 프로그램 스토어 열기
		</span>
	</section>

	<section>
		<h2>Prettier 설치</h2>

		<img src={VSCodePrettier} alt="" />
		<span class="text-4xl">코드를 깔끔하게 유지해주는 도구 설치</span>
	</section>

	<section>
		<h2>Git Extension Pack 설치</h2>

		<img src={VSCodeGitExtensionPack} alt="" />
		<span class="text-4xl">Git을 쉽게 사용하기 위한 도구들 설치</span>
	</section>

	<section>
		<h2>Prettier 설정</h2>

		<img src={VSCodePrettierSetup} alt="" />
		<span class="text-4xl">복사 붙여넣기, 저장할 때마다 코드를 깔끔하게</span>
	</section>
</section>

<!-- HTML, CSS, JS, TS 역할 -->

<section>
	<section class="!flex flex-col place-items-center justify-center gap-4">
		<h2 class="flex w-fit flex-row place-items-center justify-center gap-4">
			<img src={HTMLIcon} alt="" />

			HTML
		</h2>
	</section>

	<section>
		<h2>HTML의 역할</h2>

		<ul class="text-3xl leading-snug">
			<li class="fragment">웹 페이지의 골조 역할</li>
			<li class="fragment">사진, 글, 영상, 메뉴 등이 어디에 있어야 하는 지 표현</li>
		</ul>
	</section>
</section>

<section>
	<section class="!flex flex-col place-items-center justify-center gap-4">
		<h2 class="flex w-fit flex-row place-items-center justify-center gap-4">
			<img src={CSSIcon} alt="" />

			CSS
		</h2>
	</section>

	<section>
		<h2>CSS의 역할</h2>

		<ul class="text-3xl leading-snug">
			<li class="fragment">
				웹 페이지 내의 모든 시각적인 요소(색, 크기, 굵기, 페이지 구조, 애니메이션 등)의 세부적인
				표현을 담당
			</li>
			<li class="fragment">HTML에서 정의한 사진, 영상, 글 등의 위치와 속성을 바꿀 수 있음</li>
		</ul>
	</section>
</section>

<section>
	<section class="!flex flex-col place-items-center justify-center gap-4">
		<h2 class="flex w-fit flex-row place-items-center justify-center gap-4">
			<img src={JSIcon} alt="" />

			JavaScript
		</h2>
	</section>

	<section>
		<h2>JavaScript의 역할</h2>

		<ul class="text-3xl leading-snug">
			<li class="fragment">
				웹 페이지 내의 모든 동적(키보드, 마우스 입력 처리, 수학 연산 등)인 요소를 담당
			</li>
			<li class="fragment">DOM을 사용해 CSS나 HTML을 조작도 가능</li>
		</ul>
	</section>
</section>

<section>
	<section class="!flex flex-col place-items-center justify-center gap-4">
		<h2 class="flex w-fit flex-row place-items-center justify-center gap-4">
			<img src={TSIcon} alt="" />

			TypeScript
		</h2>
	</section>

	<section>
		<h2>TypeScript의 역할</h2>

		<ul class="text-3xl leading-snug">
			<li class="fragment">타입, 자료형의 추가를 통한 JavaScript의 보완제 역할</li>
			<li class="fragment">
				JavaScript는 숫자, 문자, 집합 등의 타입이 개념상으로만 존재해서, <br />
				실수로 숫자와 문자를 곱하는 등의 명령을 쓰면 오류가 발생함
			</li>
			<li class="fragment">이러한 타입 관련 오류를 해결하기 위해 등장한 언어</li>
			<li class="fragment">
				"아무리 뛰어난 개발자라도 수백만 줄의 코드의 타입을 정확하게 실수 없이 다룰 수는 없음"
			</li>
		</ul>
	</section>

	<section>
		<h2>TypeScript가 고치는 문제들</h2>

		<pre><code data-trim data-noescape class="language-js">
			console.log(1 + "2"); // {1 + '2'}
			console.log(undefined === null); // {undefined === null}
			console.log(null + 3); // {null + 3}
			console.log(('b'+'a'+ +'a'+'a').toLowerCase()); // {('b' + 'a' + +'a' + 'a').toLowerCase()}

			let x;
			console.log(!x); // {!undefined}
		</code></pre>

		<span class="fragment text-4xl">
			타입스크립트는 타입 관련 오류를 상세하게 출력함. <br />
			자바스크립트는 오류 로그 출력 없이, 그냥 실행함
		</span>
	</section>
</section>

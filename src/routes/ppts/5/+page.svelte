<section class="!flex flex-col place-items-center">
	<h2>TypeScript 프로젝트 설정</h2>

	<img src="/icons8-typescript-96.png" alt="" width="144" />
</section>

<section>
	<h2>#1 프로젝트 생성</h2>

	<pre><code data-trim data-noescape class="language-bash">
    <script type="text/template">
      # 패키지 관리자에 따라 다음 명령을 통해 프로젝트를 생성할 수 있습니다
      # .을 입력하면 현재 경로로 인식합니다 (예시: "pnpm init .")
      npm init <경로>
      yarn init <경로>
      pnpm init <경로>
			</script>
    </code></pre>
</section>

<section>
	<section>
		<h2>#2 필수 라이브러리 설치</h2>

		<span class="r-fit-text">
			타입스크립트 실행을 위해서는 <u>typescript</u>, <u>@types/node</u>, <u>ts-node</u>가
			필요합니다.
			<br />
			아래 명령은 개발에만 사용되는 라이브러리를 구분하여 설치합니다
		</span>

		<pre><code data-trim data-noescape class="language-bash">
    <script type="text/template">
      pnpm i typescript  # 일반 설치
      pnpm i -D @types/node ts-node  # 개발용 설치
				</script>
    </code></pre>
	</section>

	<section>
		<h2>각 라이브러리의 역할</h2>
	</section>
</section>

<section>
	<h2>#3 <u>tsconfig.json</u> 설정</h2>

	<pre><code data-trim data-noescape class="language-bash">
		# 아래 명령을 통해 타입스크립트 기본 설정을 생성할 수 있습니다
		tsc --init
    </code></pre>
</section>

<section>
	<h2>타입스크립트 실행하는 법</h2>

	<pre><code data-trim data-noescape class="language-bash">
    <script type="text/template">
		# 아래 명령으로 실행 가능 (예시: pnpm ts-node ./index.ts)
		pnpm ts-node <타입스크립트 경로>
			</script>
	</code></pre>
</section>

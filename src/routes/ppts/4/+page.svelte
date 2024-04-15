<script lang="ts">
	import NodeJSIcon from './files/icons8-nodejs-144.png';
	import NPMIcon from './files/icons8-npm-144.png';

	import NVMWindowsSearchResultImage from './files/nvm-windows-search-result-from-google.png';
	import NVMWindowsReleasesPageImage from './files/nvm-windows-search-result-from-google.png';
	import NVMSetupDownloadLinkImage from './files/nvm-setup-image.png';
</script>

<section class="!flex flex-col place-items-center justify-center gap-4">
	<h2 class="r-fit-text">JavaScript 개발 환경 설정</h2>
	<img src={NodeJSIcon} alt="" width="144" />
</section>

<!-- NVM 설치 -->
<section>
	<section class="!flex flex-col place-items-center justify-center gap-4">
		<h2 class="r-fit-text">Node.js 개발 환경 설정 #1: nvm 설치하기</h2>

		<span class="text-4xl">내가 원하는 Node.js 버전 빨리 설정하기</span>

		<img src={NodeJSIcon} alt="" width="144" />
	</section>

	<section class="!flex flex-col place-items-center justify-center gap-4">
		<h2>nvm 설치 파일 다운로드하기 #1</h2>

		<p class="text-3xl">
			Google에서 <a href="https://github.com/coreybutler/nvm-windows">nvm-windows (GitHub)</a>를
			검색하세요
		</p>

		<img src={NVMWindowsSearchResultImage} alt="" />
	</section>

	<section class="!flex flex-col place-items-center justify-center gap-4">
		<h2>nvm 설치 파일 다운로드하기 #2</h2>

		<p class="text-3xl">
			<a href="https://github.com/coreybutler/nvm-windows">nvm-windows</a> GitHub 페이지에서
			<a href="https://github.com/coreybutler/nvm-windows/releases">Download Now!</a>를 찾아
			들어가세요
		</p>

		<img src={NVMWindowsReleasesPageImage} alt="" />
	</section>

	<section class="!flex flex-col place-items-center justify-center gap-4">
		<h2>nvm 설치 파일 다운로드하기 #3</h2>

		<p class="text-3xl">
			최신 버전의 <u>nvm-setup.exe</u>를 다운로드 하고 설치 작업을 완료하세요
		</p>

		<img src={NVMSetupDownloadLinkImage} alt="" />
	</section>
</section>

<!-- NVM으로 Node.js 다운로드하기 -->
<section>
	<section class="!flex flex-col place-items-center justify-center gap-4">
		<h2 class="r-fit-text">Node.js 개발 환경 설정 #2: NVM으로 Node.js 설치하기</h2>

		<img src={NodeJSIcon} alt="" width="144" />
	</section>

	<section>
		<h2>nvm 설치 확인하기</h2>

		<pre><code data-trim data-noescape class="language-bash">
      nvm --version  # nvm 버전 확인 명령어
    </code></pre>

		<p class="text-3xl">결과 예시</p>

		<pre><code data-trim data-noescape class="language-bash">
      <script type="text/template">
      C:\Users\devcomfort>nvm --version
      1.1.11
				</script>
    </code></pre>
	</section>

	<section>
		<h2 class="r-fit-text">nvm으로 설치할 수 있는 Node.js 리스트 보기</h2>

		<pre><code data-trim data-noescape class="language-bash">
      nvm list available  # '설치 가능한' Node.js 목록 표시 명령어
    </code></pre>

		<p class="text-3xl">결과 예시</p>

		<pre><code data-trim data-noescape class="language-bash">
      <script type="text/template">
        C:\Users\devcomfort>nvm list available

        |   CURRENT    |     LTS      |  OLD STABLE  | OLD UNSTABLE |
        |--------------|--------------|--------------|--------------|
        |    21.7.3    |   20.12.2    |   0.12.18    |   0.11.16    |
        |    21.7.2    |   20.12.1    |   0.12.17    |   0.11.15    |
        |    21.7.1    |   20.12.0    |   0.12.16    |   0.11.14    |
        |    21.7.0    |   20.11.1    |   0.12.15    |   0.11.13    |
        |    21.6.2    |   20.11.0    |   0.12.14    |   0.11.12    |
        |    21.6.1    |   20.10.0    |   0.12.13    |   0.11.11    |
        |    21.6.0    |    20.9.0    |   0.12.12    |   0.11.10    |
        |    21.5.0    |   18.20.2    |   0.12.11    |    0.11.9    |
        |    21.4.0    |   18.20.1    |   0.12.10    |    0.11.8    |
        |    21.3.0    |   18.20.0    |    0.12.9    |    0.11.7    |
        |    21.2.0    |   18.19.1    |    0.12.8    |    0.11.6    |
        |    21.1.0    |   18.19.0    |    0.12.7    |    0.11.5    |
        |    21.0.0    |   18.18.2    |    0.12.6    |    0.11.4    |
        |    20.8.1    |   18.18.1    |    0.12.5    |    0.11.3    |
        |    20.8.0    |   18.18.0    |    0.12.4    |    0.11.2    |
        |    20.7.0    |   18.17.1    |    0.12.3    |    0.11.1    |
        |    20.6.1    |   18.17.0    |    0.12.2    |    0.11.0    |
        |    20.6.0    |   18.16.1    |    0.12.1    |    0.9.12    |
        |    20.5.1    |   18.16.0    |    0.12.0    |    0.9.11    |
        |    20.5.0    |   18.15.0    |   0.10.48    |    0.9.10    |

        This is a partial list. For a complete list, visit https://nodejs.org/en/download/releases
				</script>
    </code></pre>
	</section>

	<section>
		<h2>nvm으로 Node.js 설치하기</h2>

		<span class="text-2xl">
			원하는 Node.js를 찾아 설치하세요. 최신 버전은 사용할 라이브러리와 호환이 안 될 수 있고, LTS
			버전은 상대적으로 호환성이 뛰어납니다.
		</span>

		<pre><code data-trim data-noescape class="language-bash">
      <script type="text/template">
      nvm install <버전 정보>  # 특정 버전 설치 명령어
				</script>
    </code></pre>

		<p class="text-2xl">실행 예시</p>

		<pre><code data-trim data-noescape class="language-bash">
      <script type="text/template">
			C:\Users\devcomfort>nvm install 18 --lts
			Downloading node.js version 18.20.2 (64-bit)...
			Extracting node and npm...
			Complete
			npm v10.5.0 installed successfully.


			Installation complete. If you want to use this version, type

			nvm use 18.20.2
				</script>
    </code></pre>
	</section>
</section>

<!-- NVM에서 특정 버전 활성화하기 -->
<section>
	<section class="!flex flex-col place-items-center justify-center gap-4">
		<h2 class="r-fit-text">Node.js 개발 환경 설정 #3: NVM으로 Node.js 활성화하기</h2>

		<img src={NodeJSIcon} alt="" width="144" />
	</section>

	<section>
		<h2>nvm으로 원하는 버전 활성화하기</h2>

		<pre><code data-trim data-noescape class="language-bash">
      <script type="text/template">
      nvm use <버전 정보>  # 해당 버전을 활성화합니다
				</script>
    </code></pre>

		<p class="text-2xl">실행 예시</p>

		<pre><code data-trim data-noescape class="language-bash">
      <script type="text/template">
			C:\Users\devcomfort>nvm use 18.20.2
			Now using node v18.20.2 (64-bit)
				</script>
    </code></pre>
	</section>

	<section>
		<h2>현재 활성화 된 버전 확인하기</h2>

		<pre><code data-trim data-noescape class="language-bash">
      <script type="text/template">
      nvm current  # 현재 활성화된 Node.js 버전을 확인합니다
				</script>
    </code></pre>

		<p class="text-2xl">실행 예시</p>

		<pre><code data-trim data-noescape class="language-bash">
      <script type="text/template">
			C:\Users\devcomfort>nvm current
			v18.20.2
				</script>
    </code></pre>
	</section>
</section>

<section>
	<section>
		<h2 class="r-fit-text !flex w-fit flex-col place-items-center justify-center gap-4">
			패키지 관리자 알아보기 + 설치하기

			<img src={NPMIcon} alt="" />
		</h2>
	</section>

	<section>
		<h2>패키지 관리자란?</h2>

		<p class="r-fit-text">
			프로젝트와 관련된 패키지, 라이브러리를 쉽게 설치하거나 제거할 수 있도록 <br />
			여러 기능을 지원하는 도구 또는 프로그램 <br /><br />
			간혹 프로젝트 관리를 위한 기능이 포함되기도 함
		</p>
	</section>

	<section>
		<h2>npm vs yarn vs pnpm</h2>

		<ul class="r-fit-text">
			<li>
				npm: 최초의 패키지 관리자. 느림, 보안 이슈나 호환성 문제가 있음. <br />
				: 보안 경고로 인해 라이브러리가 설치되지 않는 경우가 있음
			</li>
			<li>
				yarn(classic): npm의 호환성 이슈와 속도를 개선한 패키지 관리자 <br />
				: 기본에 충실한 패키지 관리자
			</li>
			<li>
				yarn(berry): 자체 개발한 캐싱 기능을 통해 적은 공간만 사용, node_modules 없음 <br />
				: 자체 개발한 캐싱 기능 때문에 라이브러리가 호환되지 않는 경우가 있음
			</li>
			<li>
				pnpm: 빠름, 심볼릭 링크를 적극적으로 활용하여 적은 공간만 사용 <br />
				: 최적화된 npm
			</li>
		</ul>
	</section>

	<section>
		<h2>패키지 관리자 설치 방법</h2>

		<ul class="r-fit-text">
			<li>npm: Node.js를 설치하면 기본으로 설치됨</li>
			<li>yarn(classic): <u>npm i -g yarn</u> 실행</li>
			<li>yarn(berry): yarn(classic) 설치 후, <u>yarn set version berry</u> 입력</li>
			<li>pnpm: <u>npm i -g pnpm</u> 실행</li>
		</ul>
	</section>
</section>

<script lang="ts">
	import '@picocss/pico/css/pico.css';
  import {format} from 'date-fns'

  const pptList = [
    {
      title:"Orientation",
      body: "수업 관련 안내 사항 전달",
      date: new Date("2024-04-08"),
      link: "./ppts/1"
    }
  ] as const;
</script>

<div>
	<main class="container fluid-width">
    <hgroup>
      <p class="font-bold text-4xl">PPT List</p>
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
          <td>{format(ppt.date, "yyyy.MM.dd")}</td>
          <td>
            <a href="{ppt.link}">접속하기</a>
          </td>
        </tr>
        {/each}
      </tbody>
    </table>
  </main>
</div>

<script>
  let kana = [
    {
      name: "첫 번째",
      num: '01',
    },
    {
      name: "두 번째",
      num: '02',
    },
    {
      name: "세 번째",
      num: '03',
    },
  ]

  let count = 0; // count는 변수명, 0은 초기값
  function incrementCount() { //function 다음 써지는 이름은 기능 이름임.
    count += 1;
  }
</script>

<main>
  <div class="container">
    {#each kana as list, i } <!-- each는 반복문, list는 반복되는 요소, i는 인덱스 -->
      <p>{i}: { list.name }</p>
      <p>{ list.num }</p>
    {/each}
    <div class="array">
      {#each Array(20) as _, i}
        <p>아무거나</p>
      {/each}
    </div>
    <h4>{ count }</h4>
    <button on:click={ incrementCount }>클릭 수: { count }</button> <!-- 버튼을 누르면 카운트 됨 -->
  </div>
</main>

<style>
  .container {
    width: 100%;
    display: flex;
    flex-direction: column;
  }
  .array {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }
</style>

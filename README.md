[window_brand_case_study.html](https://github.com/user-attachments/files/28507041/window_brand_case_study.html)
<!doctype html>
<html lang="ko">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>창호 브랜드 선택 시뮬레이션 케이스 스터디</title>
<style>
:root{
  --navy:#0B1F4D; --blue:#0B5FA5; --sky:#EAF3FF; --teal:#0F766E;
  --gray:#F5F7FA; --line:#D8E2EF; --text:#1F2937; --muted:#6B7280;
  --orange:#EA580C; --green:#0F766E; --purple:#5B5BD6;
}
*{box-sizing:border-box}
body{margin:0;background:#f3f6fb;font-family:"Noto Sans KR","Noto Sans CJK KR","Malgun Gothic",Arial,sans-serif;color:var(--text);line-height:1.58}
.wrap{max-width:1180px;margin:34px auto;background:white;border:1px solid #dfe8f4;border-radius:24px;box-shadow:0 16px 38px rgba(11,31,77,.12);overflow:hidden}
header{padding:44px 56px 34px;background:linear-gradient(135deg,#fff 0%,#edf6ff 100%);border-bottom:1px solid var(--line)}
.badge{display:inline-flex;align-items:center;gap:8px;background:var(--navy);color:#fff;border-radius:999px;padding:7px 14px;font-weight:800;font-size:14px}
h1{margin:22px 0 9px;color:var(--navy);font-size:38px;letter-spacing:-.045em;line-height:1.17}
.sub{margin:0;color:#374151;font-size:19px;letter-spacing:-.02em}
.summary{display:grid;grid-template-columns:repeat(3,1fr);gap:15px;margin-top:26px}
.summary .card{background:#fff;border:1px solid var(--line);border-radius:18px;padding:18px 20px;box-shadow:0 8px 20px rgba(16,47,91,.06)}
.summary b{display:block;color:var(--blue);font-size:14px;margin-bottom:6px}
.summary span{display:block;color:var(--navy);font-size:20px;font-weight:900;letter-spacing:-.035em}
main{padding:42px 56px 54px}
.section-title{margin:0 0 18px;display:flex;align-items:center;gap:12px;color:var(--navy);font-size:26px;letter-spacing:-.04em}
.num{width:38px;height:38px;border-radius:13px;background:var(--blue);color:white;display:inline-flex;align-items:center;justify-content:center;font-weight:900}
.case{border:1px solid var(--line);border-radius:24px;background:white;overflow:hidden;margin:0 0 32px;box-shadow:0 10px 22px rgba(16,47,91,.05)}
.case-head{padding:24px 28px;background:linear-gradient(135deg,#0b3a75,#0b5fa5);color:white;display:flex;justify-content:space-between;gap:24px;align-items:flex-start}
.case-head h2{margin:0;font-size:27px;letter-spacing:-.045em;line-height:1.25}
.case-head p{margin:7px 0 0;color:#dceeff;font-size:15px}
.tag{white-space:nowrap;border:1px solid rgba(255,255,255,.45);background:rgba(255,255,255,.14);color:#fff;border-radius:999px;padding:7px 12px;font-size:14px;font-weight:800}
.case-body{padding:28px;display:grid;grid-template-columns:1fr 1fr;gap:22px}
.block{border:1px solid #e5edf7;border-radius:18px;background:#f8fafc;padding:20px 22px}
.block.full{grid-column:1/-1}
.block h3{margin:0 0 12px;color:var(--blue);font-size:18px;letter-spacing:-.03em}
p{margin:0 0 10px} p:last-child{margin-bottom:0}
table{width:100%;border-collapse:separate;border-spacing:0;border:1px solid var(--line);border-radius:16px;overflow:hidden;background:#fff;font-size:15px}
th{background:#0b3a75;color:#fff;text-align:left;padding:12px 14px;font-weight:900}
td{padding:13px 14px;border-top:1px solid var(--line);vertical-align:top}
tr:nth-child(even) td{background:#fafcff}
.flow{display:grid;grid-template-columns:1fr auto 1fr;gap:12px;align-items:center;margin-top:8px}
.brand{border:1px solid #cddced;background:white;border-radius:16px;padding:18px;text-align:center}
.brand .name{font-size:28px;font-weight:900;color:var(--navy)}
.brand .desc{font-size:14px;color:#4b5563;margin-top:6px}
.vs{width:48px;height:48px;border-radius:50%;background:var(--sky);color:var(--blue);display:flex;align-items:center;justify-content:center;font-weight:900;border:1px solid #bdd8f3}
.choice{background:#edf7f6;border-color:#bfe1dc}
.choice h3{color:var(--green)}
.warn{background:#fff7ed;border-color:#fed7aa}
.warn h3{color:var(--orange)}
.quote{background:white;border-left:5px solid var(--blue);border-radius:14px;padding:14px 17px;font-weight:800;color:#111827;margin:12px 0}
.kpi{display:grid;grid-template-columns:repeat(4,1fr);gap:12px;margin-top:10px}
.kpi div{background:white;border:1px solid var(--line);border-radius:14px;padding:14px;text-align:center}
.kpi b{display:block;color:var(--blue);font-size:13px}
.kpi span{display:block;color:var(--navy);font-size:22px;font-weight:900;margin-top:3px}
.conclusion{margin-top:36px;border-radius:24px;background:linear-gradient(135deg,#0b1f4d,#0b5fa5);color:#eaf3ff;padding:30px 34px}
.conclusion h2{margin:0 0 12px;color:white;font-size:28px;letter-spacing:-.04em}
.conclusion p{font-size:18px}
.footer{padding:20px 56px;border-top:1px solid var(--line);background:#fafcff;color:var(--muted);font-size:13px}
@media(max-width:900px){.wrap{margin:0;border-radius:0}header,main,.footer{padding-left:24px;padding-right:24px}.summary,.case-body,.kpi{grid-template-columns:1fr}.block.full{grid-column:auto}.case-head{flex-direction:column}.tag{white-space:normal}.flow{grid-template-columns:1fr}.vs{margin:auto}}
</style>
</head>
<body>
<div class="wrap">
<header>
  <span class="badge">소비자 의사결정 시뮬레이션</span>
  <h1>창호 브랜드 선택 케이스 스터디</h1>
  <p class="sub">RAW DATA 기반으로 본 소비자의 비교 브랜드, 판단 기준, 선택 압력</p>
  <div class="summary">
    <div class="card"><b>핵심 질문 1</b><span>1군 브랜드끼리 비교 시<br>무엇이 KCC 선택을 만드는가</span></div>
    <div class="card"><b>핵심 질문 2</b><span>기타 브랜드 대비<br>KCC 프리미엄은 어디까지 가능한가</span></div>
    <div class="card"><b>핵심 질문 3</b><span>가격·보증·후기·할부가<br>선택을 어떻게 바꾸는가</span></div>
  </div>
</header>

<main>
<h2 class="section-title"><span class="num">1</span>케이스별 의사결정 시뮬레이션</h2>

<section class="case">
  <div class="case-head">
    <div>
      <h2>CASE 1. LX vs KCC 검토 후 LX 선택</h2>
      <p>거주중 시공·어린 자녀·시공 리스크가 큰 상황</p>
    </div>
    <span class="tag">최종 선택 확인: LX</span>
  </div>
  <div class="case-body">
    <div class="block">
      <h3>비교 브랜드</h3>
      <div class="flow">
        <div class="brand"><div class="name">LX</div><div class="desc">본사 직계약 · 완성창 · 시공 관리</div></div>
        <div class="vs">VS</div>
        <div class="brand"><div class="name">KCC</div><div class="desc">1군 브랜드 · 제품 신뢰 후보</div></div>
      </div>
    </div>
    <div class="block">
      <h3>소비자 상황</h3>
      <p>50평형 구축 아파트, 어린 자녀 2명 거주, 아이 방 외풍 문제로 창호 교체를 검토했다. 거주중 시공이므로 보양, 먼지, 냄새, 기존 인테리어 손상 우려가 컸다.</p>
    </div>
    <div class="block full">
      <h3>판단 기준</h3>
      <table>
        <tr><th>판단 기준</th><th>소비자 반응</th></tr>
        <tr><td>본사 직계약 여부</td><td>LX 본사 직계약에 안정감을 느낌</td></tr>
        <tr><td>거주중 시공 리스크</td><td>보양, 마감, 기존 인테리어 손상 최소화가 중요</td></tr>
        <tr><td>아이 있는 집의 안전성</td><td>실리콘 냄새, 청소, 당일 생활 가능 여부 확인</td></tr>
        <tr><td>제품보다 관리 체계</td><td>제품 성능뿐 아니라 상담·실측·시공·마감까지 관리되는 구조를 중시</td></tr>
      </table>
    </div>
    <div class="block full choice">
      <h3>시뮬레이션 문장</h3>
      <p class="quote">“KCC도 믿을 만한 브랜드지만, 아이가 있는 거주중 시공이라면 조금 더 비싸더라도 본사 직계약과 시공 관리 체계가 명확한 LX를 선택한다.”</p>
    </div>
  </div>
</section>

<section class="case">
  <div class="case-head">
    <div>
      <h2>CASE 2. KCC vs PNS 비교 시 KCC 선택 압력 우세</h2>
      <p>1군 브랜드 신뢰와 후기·가격·프로모션 기반 대안의 비교</p>
    </div>
    <span class="tag">댓글 반응 기준: KCC 우세</span>
  </div>
  <div class="case-body">
    <div class="block">
      <h3>비교 브랜드</h3>
      <div class="flow">
        <div class="brand"><div class="name">KCC</div><div class="desc">1군 브랜드 · 제품 신뢰 · 장기 안정성</div></div>
        <div class="vs">VS</div>
        <div class="brand"><div class="name">PNS</div><div class="desc">가격 대안 · 후기 기반 신뢰 · 프로모션</div></div>
      </div>
    </div>
    <div class="block">
      <h3>소비자 상황</h3>
      <p>작성자는 KCC 견적과 PNS 견적을 비교하며, “브랜드 가격이고 창은 다 비슷비슷한데 시공이 제일 중요하다”는 인식 속에서 실제 선택 기준을 확인하려 했다.</p>
    </div>
    <div class="block full">
      <h3>판단 기준</h3>
      <table>
        <tr><th>판단 기준</th><th>소비자 반응</th></tr>
        <tr><td>브랜드 신뢰도</td><td>KCC가 우위</td></tr>
        <tr><td>제품 안정성</td><td>장기 사용 제품이므로 1군 브랜드 선호 작동</td></tr>
        <tr><td>가격 차이</td><td>가격 차이가 크지 않으면 KCC 선택 압력 강화</td></tr>
        <tr><td>후기·프로모션</td><td>PNS는 후기량, 지인 소개, 상품권 이벤트 등으로 신뢰 보완 가능</td></tr>
        <tr><td>시공능력</td><td>브랜드와 별개로 실제 시공 품질이 중요하다는 인식 유지</td></tr>
      </table>
    </div>
    <div class="block full choice">
      <h3>시뮬레이션 문장</h3>
      <p class="quote">“PNS가 후기와 프로모션으로 신뢰를 보완하더라도, 가격 차이가 크지 않다면 장기 사용 안정성과 1군 브랜드 신뢰를 고려해 KCC를 선택한다.”</p>
    </div>
  </div>
</section>

<section class="case">
  <div class="case-head">
    <div>
      <h2>CASE 3. KCC 대리점창 vs 현대L&C</h2>
      <p>브랜드 신뢰와 무이자 할부 조건의 충돌</p>
    </div>
    <span class="tag">선택 유인 발생: 현대L&C</span>
  </div>
  <div class="case-body">
    <div class="block">
      <h3>비교 브랜드</h3>
      <div class="flow">
        <div class="brand"><div class="name">KCC</div><div class="desc">대리점창 · 1군 브랜드 신뢰</div></div>
        <div class="vs">VS</div>
        <div class="brand"><div class="name">현대L&C</div><div class="desc">1군 대안 · 무이자 할부</div></div>
      </div>
    </div>
    <div class="block">
      <h3>소비자 상황</h3>
      <p>현대L&C 견적이 KCC 대리점창보다 조금 비쌌지만, 무이자 할부 조건에 크게 반응했다. 창호 비용을 카드로 결제하면 현금을 다른 인테리어 공정에 활용할 수 있다고 판단했다.</p>
    </div>
    <div class="block full">
      <h3>판단 기준</h3>
      <table>
        <tr><th>판단 기준</th><th>소비자 반응</th></tr>
        <tr><td>총 견적 금액</td><td>현대L&C가 KCC보다 조금 비쌈</td></tr>
        <tr><td>결제 조건</td><td>무이자 할부가 큰 매력</td></tr>
        <tr><td>현금 유동성</td><td>창호를 카드로 처리하면 인테리어 예산 운용이 편해짐</td></tr>
        <tr><td>브랜드 신뢰</td><td>현대L&C도 1군인지 확인하고자 함</td></tr>
        <tr><td>구매 부담</td><td>총액보다 월 부담과 현금 여력에 반응</td></tr>
      </table>
    </div>
    <div class="block full choice">
      <h3>시뮬레이션 문장</h3>
      <p class="quote">“KCC가 더 익숙한 브랜드라도, 현대L&C가 무이자 할부를 제공한다면 전체 인테리어 예산 운용 측면에서 현대L&C를 선택할 수 있다.”</p>
    </div>
  </div>
</section>

<section class="case">
  <div class="case-head">
    <div>
      <h2>CASE 4. LX 본사창 vs LX 직영창</h2>
      <p>본사 책임과 20% 이상 가격 차이의 비교</p>
    </div>
    <span class="tag">최종 선택 확인: 직영창</span>
  </div>
  <div class="case-body">
    <div class="block">
      <h3>비교 채널</h3>
      <div class="flow">
        <div class="brand"><div class="name">LX 본사창</div><div class="desc">본사 책임 · 안정성 · 신뢰</div></div>
        <div class="vs">VS</div>
        <div class="brand"><div class="name">LX 직영창</div><div class="desc">동일 브랜드 기반 · 가격 경쟁력</div></div>
      </div>
    </div>
    <div class="block">
      <h3>소비자 상황</h3>
      <p>32평 구축 일부 창호 교체 사례에서 LX 본사창과 직영창 사이를 마지막까지 고민했다. 본사창과 직영창의 가격 차이가 20% 이상 발생했고, 부품을 일일이 비교한 뒤 직영창을 선택했다.</p>
    </div>
    <div class="block full">
      <h3>판단 기준</h3>
      <table>
        <tr><th>판단 기준</th><th>소비자 반응</th></tr>
        <tr><td>브랜드 신뢰</td><td>LX라는 브랜드 자체는 유지</td></tr>
        <tr><td>가격 차이</td><td>본사창 대비 직영창이 20% 이상 저렴</td></tr>
        <tr><td>부품 비교 가능성</td><td>부품을 일일이 비교 후 직영창 선택</td></tr>
        <tr><td>시공 만족도</td><td>실제 시공 인력은 프로라고 평가</td></tr>
        <tr><td>영업 응대</td><td>영업 담당자는 별로였으나 시공 결과가 만족도를 상쇄</td></tr>
      </table>
    </div>
    <div class="block full choice">
      <h3>시뮬레이션 문장</h3>
      <p class="quote">“본사창이 더 안전해 보이지만, 20% 이상 가격 차이가 나고 부품·사양이 납득된다면 더 합리적인 직영창을 선택한다.”</p>
    </div>
  </div>
</section>

<section class="case">
  <div class="case-head">
    <div>
      <h2>CASE 5. KCC 견적이 LX 완성창 수준으로 인식될 때</h2>
      <p>KCC 가격 프리미엄에 대한 소비자 저항 구간</p>
    </div>
    <span class="tag">최종 선택: 확인 불가</span>
  </div>
  <div class="case-body">
    <div class="block">
      <h3>비교 기준</h3>
      <div class="flow">
        <div class="brand"><div class="name">KCC</div><div class="desc">VBF242 · 로이그린 24T · 1군 브랜드</div></div>
        <div class="vs">VS</div>
        <div class="brand"><div class="name">LX 완성창 기준</div><div class="desc">고가이나 본사 책임이면 가격 납득 가능</div></div>
      </div>
    </div>
    <div class="block">
      <h3>소비자 상황</h3>
      <p>KCC VBF242, 로이그린 24T 적용, 샷시 4개와 터닝도어 1개 견적이 1,169만 원(부가세 별도)으로 제시되었다. 소비자는 1천만 원 이내를 예상했으나 가격이 높다고 느꼈다.</p>
    </div>
    <div class="block full">
      <h3>댓글 반응 및 판단 기준</h3>
      <table>
        <tr><th>판단 기준</th><th>소비자 반응</th></tr>
        <tr><td>가격 저항</td><td>KCC로는 비싸게 느껴진다는 반응</td></tr>
        <tr><td>LX와의 비교</td><td>“LX 완성창이면 이해되지만 KCC로는…”이라는 가격 저항 발생</td></tr>
        <tr><td>비교견적 필요성</td><td>2~3곳 비교견적 권유</td></tr>
        <tr><td>포함 항목</td><td>자동핸들, 방충망 포함 여부만으로 가격 저항을 완전히 해소하지 못함</td></tr>
        <tr><td>최종 선택</td><td>작성자의 최종 선택은 확인되지 않음</td></tr>
      </table>
    </div>
    <div class="block full warn">
      <h3>시뮬레이션 문장</h3>
      <p class="quote">“KCC는 믿을 만한 브랜드지만, 가격이 LX 완성창 수준까지 올라가면 소비자는 바로 비교견적을 찾는다. 이때 KCC가 선택되려면 LX 대비 가격 메리트가 있거나, 정품·사양·보증·A/S 책임 구조가 명확히 설명되어야 한다.”</p>
    </div>
  </div>
</section>

<h2 class="section-title"><span class="num">2</span>케이스 종합 비교</h2>
<table>
  <tr><th>케이스</th><th>비교 브랜드 / 채널</th><th>소비자 핵심 고민</th><th>선택 또는 선택 압력</th><th>결정 요인</th></tr>
  <tr><td><b>CASE 1</b></td><td>LX vs KCC</td><td>거주중 시공, 아이 있는 집, 시공 리스크</td><td><b>LX 선택</b></td><td>본사 직계약, 상담·실측 신뢰, 시공 관리 체계</td></tr>
  <tr><td><b>CASE 2</b></td><td>KCC vs PNS</td><td>1군 브랜드 신뢰 vs 후기·가격·프로모션 기반 대안</td><td><b>KCC 선택 압력 우세</b></td><td>브랜드 신뢰, 제품 안정성, 가격 차이 제한적</td></tr>
  <tr><td><b>CASE 3</b></td><td>KCC 대리점창 vs 현대L&C</td><td>KCC 신뢰 vs 현대L&C 무이자 할부</td><td><b>현대L&C 선택 유인 발생</b></td><td>무이자 할부, 현금 유동성, 구매 부담 완화</td></tr>
  <tr><td><b>CASE 4</b></td><td>LX 본사창 vs LX 직영창</td><td>본사 책임 vs 20% 이상 가격 차이</td><td><b>직영창 선택</b></td><td>사양 비교 가능, 가격 경쟁력, 시공 만족</td></tr>
  <tr><td><b>CASE 5</b></td><td>KCC vs LX 완성창 기준 가격</td><td>KCC 견적이 비싸게 느껴질 때</td><td><b>비교견적 단계로 전환</b></td><td>가격 저항, 보증·사양 설명 필요</td></tr>
</table>

<div class="conclusion">
  <h2>KCC 관점 핵심 결론</h2>
  <p>소비자는 창호 브랜드를 단순히 이름값으로 선택하지 않는다. LX는 본사 책임과 시공 관리 체계가 명확할 때 선택되고, KCC는 기타 브랜드 대비 가격 차이가 크지 않을 때 1군 브랜드 신뢰로 선택 압력이 높아진다. 반면 KCC 가격이 LX 완성창 수준까지 올라가면 소비자는 즉시 비교견적을 찾으며, 현대L&C처럼 무이자 할부를 제공하거나 PNS처럼 후기·추천 프로모션을 강화한 브랜드도 충분히 대안으로 인식된다.</p>
</div>
</main>
<div class="footer">자료: 대화 내 RAW DATA 및 소비자 댓글 반응 기반 시뮬레이션 정리</div>
</div>
</body>
</html>

# Reading 40: Security Market Indexes (증권시장 지수)

> **핵심 질문:** 주가지수는 어떻게 만들어지고, 어떤 가중 방식이 있으며, 어떻게 활용되는가?

---

## 왜 증권시장 지수를 이해해야 하는가?

올림픽에서 "한국 팀 전체 성적"을 나타내려면 금·은·동메달을 어떻게 합산할지 결정해야 합니다. 주가지수도 마찬가지입니다. 수천 개의 주식 성과를 하나의 숫자로 요약해야 하는데, 어떻게 합산하느냐(가중 방식)에 따라 결과가 크게 달라집니다. 이 Reading에서는 지수의 구성, 계산, 활용 방법을 체계적으로 배웁니다.

---

## Module 40.1 지수 가중 방법

---

## LOS 40.a: 증권시장 지수의 정의 (Describe a security market index)

**증권시장 지수(Security Market Index)**란:
- 자산군, 증권 시장, 또는 시장 세그먼트의 **성과를 나타내는 척도**
- **구성 증권(constituent securities)**: 지수를 이루는 개별 증권들
- 구성 증권의 시장 가격(가용 시 실제가, 그렇지 않으면 추정가)으로부터 수치 산출
- **지수 수익률(index return)**: 일정 기간 동안 지수 값의 변화율(%)

---

## LOS 40.b: 지수의 가치, 가격 수익률, 총 수익률 계산 (Calculate and interpret the value, price return, and total return of an index)

### 두 가지 수익률 유형

| 구분 | 정의 | 포함 요소 |
|------|------|----------|
| **가격 수익률(Price Return)** | 가격 지수 기반 수익률 | 가격 변동만 반영 |
| **총 수익률(Total Return)** | 수익 지수 기반 수익률 | 가격 + 배당·이자 반영 |

배당이나 이자 수입이 있으면 **총 수익률 > 가격 수익률**

### 복합 기간 수익률 계산 공식

$$R_P = (1 + R_{S1})(1 + R_{S2})(1 + R_{S3}) \cdots (1 + R_{Sk}) - 1$$

| 변수 | 설명 |
|------|------|
| $R_P$ | 전체 측정 기간의 포트폴리오 수익률 |
| $k$ | 소기간(subperiod)의 수 |
| $R_{Sk}$ | $k$번째 소기간의 포트폴리오 수익률 |

> **예제: 복합 기간 수익률 계산**
>
> 첫 번째 기간 수익률: 0.50%, 두 번째 기간 수익률: 1.04%
>
> $$R_P = (1 + 0.005)(1 + 0.0104) - 1 = (1.005)(1.0104) - 1 = 0.0155 = 1.55\%$$
>
> 초기 지수값이 100이면, 두 기간 후 지수값: $100 \times 1.0155 = 101.55$

---

## LOS 40.c: 지수 구성 및 관리의 선택 사항 (Describe the choices and issues in index construction and management)

지수 제공자가 결정해야 할 사항:

1. **대상 시장(Target market):** 미국 전체 주식? 미국 소형 가치주?
2. **편입 증권 선정:** 전체 시장 또는 대표 표본? 객관적 규칙 vs. 위원회 심사
3. **가중 방식(Weighting method):** 가격가중, 동일가중, 시가총액가중, 기본적 가중 등
4. **리밸런싱 주기(Rebalancing frequency):** 목표 비중으로 주기적 조정
5. **재구성 주기(Reconstitution frequency):** 편입 증권 재검토 시기

대상 시장은 지리적 범위(미국, 신흥시장, 글로벌), 경제 섹터(경기민감주), 스타일(소형·가치주)로 정의 가능

---

## LOS 40.d: 지수 가중 방법 비교 (Compare the different weighting methods)

### 5가지 가중 방식 개요

| 가중 방식 | 기준 | 대표 지수 |
|-----------|------|----------|
| 가격가중 (Price-weighted) | 주가 | DJIA, Nikkei |
| 동일가중 (Equal-weighted) | 동일 비중 | Value Line, FT Ordinary Share |
| 시가총액가중 (Market cap-weighted) | 시가총액 | S&P 500 |
| 유동주식수조정 시가총액가중 (Float-adjusted) | 유동 시가총액 | MSCI, FTSE |
| 기본적 가중 (Fundamental-weighted) | 이익, 배당, 현금흐름 | — |

### 각 방식 상세 분석

**1. 가격가중지수 (Price-Weighted Index)**

$$\text{가격가중지수} = \frac{\text{구성 주식들의 주가 합}}{\text{분할 조정된 주식 수}}$$

- **장점:** 계산 단순
- **단점:** 고가 주식이 지수에 더 큰 영향 → 경제적 비중과 무관
- 주식 분할, 자사주 매입, 주식 배당 시 **제수(divisor)** 조정 필요
- 복제 방법: 각 주식을 동일한 **주수**만큼 보유

**2. 동일가중지수 (Equal-Weighted Index)**

- 모든 구성 종목에 **동일한 수익률 비중** 부여
- 산술 평균 수익률로 계산
- **장점:** 단순
- **단점 1:** 가격 변동 후 **주기적 리밸런싱 필요** → 거래비용 발생
- **단점 2:** 소형주를 과대가중, 대형주를 과소가중
- 복제 방법: 각 종목에 **동일한 금액** 투자

**3. 시가총액가중지수 (Market Capitalization-Weighted Index)**

$$\text{시가총액가중지수} = \frac{\text{현재 총 시가총액}}{\text{기준 기간 총 시가총액}} \times \text{기준 지수값}$$

- 각 종목 비중 = 해당 시가총액 / 전체 시가총액
- **장점:** 총 투자자 부의 변화를 가장 잘 반영, 주식 분할 시 제수 조정 불필요
- **단점:** 과대평가 주식에 더 큰 비중 → 모멘텀 전략과 유사

**4. 유동주식수조정 시가총액가중지수 (Float-Adjusted Market Cap-Weighted Index)**

- **시장 유동주식수(Market float):** 실제 투자 가능한 주식(지배주주 보유분 제외)
- **자유 유동주식수(Free float):** 외국인 투자 불가 주식도 제외
- 실제 투자 가능 비중을 더 정확히 반영

**5. 기본적 가중지수 (Fundamental-Weighted Index)**

- 이익, 배당, 현금흐름, 매출 등 펀더멘털 지표로 가중
- **장점:** 시가총액가중지수의 과대평가 편향 회피
- **특성:** 가치(value) 편향 → 고 PBR 대비 낮은 주식 과대가중

---

## LOS 40.e: 지수 값과 수익률 계산 (Calculate and analyze the value and return of an index)

### 가격가중지수 계산

$$\text{가격가중지수} = \frac{\text{구성 주가의 합}}{\text{주식 수(분할 조정)}}$$

> **예제: 가격가중지수 수익률 계산**
>
> | 주식 | 12월 31일 주가 | 1월 31일 주가 |
> |------|--------------|-------------|
> | X | $10 | $20 |
> | Y | $20 | $15 |
> | Z | $60 | $40 |
>
> **12월 31일 지수값:**
> $$\frac{10 + 20 + 60}{3} = \frac{90}{3} = 30$$
>
> **1월 31일 지수값:**
> $$\frac{20 + 15 + 40}{3} = \frac{75}{3} = 25$$
>
> **1개월 수익률:**
> $$\frac{25}{30} - 1 = -16.7\%$$

> **예제: 주식 분할 시 제수 조정**
>
> Day 1 종가: A = $10, B = $20, C = $90
>
> 가격가중지수 = $(10 + 20 + 90) / 3 = 40$
>
> **C 주식 2:1 분할 후 (Day 2 개시):**
>
> 분할 후 C 주가 = $90 / 2 = $45$
>
> 새 제수 $d$를 구하면:
> $$\frac{10 + 20 + 45}{d} = 40 \implies d = \frac{75}{40} = 1.875$$
>
> **이유:** 분할은 경제적 가치 변화가 없으므로, 지수값이 그대로 40이 되도록 제수를 줄임. 앞으로는 이 1.875를 분모로 사용.

> **예제: 가격가중 vs. 시가총액가중 비교**
>
> | 기업 | 발행 주식수(000) | 주가 | 시가총액 |
> |------|----------------|------|---------|
> | A | 100 | $100 | $10,000,000 |
> | B | 1,000 | $10 | $10,000,000 |
> | C | 20,000 | $1 | $20,000,000 |
>
> **가격가중지수 기준값:**
> $$(100 + 10 + 1) / 3 = 37$$
>
> **시나리오 1: A 주가가 $200으로 2배 상승**
>
> 가격가중지수: $(200 + 10 + 1) / 3 = 70.33$ → **+33.33 상승**
>
> 시가총액가중지수 (기준 총시가총액 = $40,000,000):
> $$\frac{100,000 \times \$200 + 1,000,000 \times \$10 + 20,000,000 \times \$1}{\$40,000,000} \times 100$$
> $$= \frac{20,000,000 + 10,000,000 + 20,000,000}{40,000,000} \times 100 = \frac{50,000,000}{40,000,000} \times 100 = 125$$
>
> **시나리오 2: C 주가가 $2로 2배 상승**
>
> 가격가중지수: $(100 + 10 + 2) / 3 = 37.33$ → **+0.33 상승 (미미)**
>
> 시가총액가중지수:
> $$\frac{100,000 \times \$100 + 1,000,000 \times \$10 + 20,000,000 \times \$2}{\$40,000,000} \times 100$$
> $$= \frac{10,000,000 + 10,000,000 + 40,000,000}{40,000,000} \times 100 = \frac{60,000,000}{40,000,000} \times 100 = 150$$
>
> **결론:**
> - 가격가중: A($100 고가)의 상승이 압도적 영향 (고가 주식 편향)
> - 시가총액가중: C(시가총액 $20M으로 최대)의 상승이 가장 큰 영향 (경제적 비중 반영)

### 동일가중지수 계산

$$\text{동일가중지수 변화율} = \frac{\text{각 주식 수익률의 합계}}{\text{주식 수}} = \text{단순 평균 수익률}$$

$$\text{새 지수값} = \text{초기 지수값} \times (1 + \text{평균 수익률})$$

> **예제: 동일가중지수 계산**
>
> | 주식 | 초기가격 | 현재가격 | 수익률 |
> |------|---------|---------|--------|
> | A | $12 | $15 | +25.0% |
> | B | $52 | $48 | -7.7% |
> | C | $38 | $45 | +18.4% |
>
> 초기 지수값: 131
>
> **평균 수익률:**
> $$\frac{25\% + (-7.7\%) + 18.4\%}{3} = \frac{35.7\%}{3} = 11.9\%$$
>
> **새 지수값:**
> $$131 \times (1 + 0.119) = 131 \times 1.119 = 146.59$$
>
> *총 수익률 지수의 경우 위 기간 동안 지급된 배당도 기간 수익률에 포함.*

---

## Module Quiz 40.1

**Q1.** Choices that must be made when constructing a security market index least likely include whether to:

A. use a nominal or interval scale.
B. measure the performance of an entire market or market segment.
C. weight the securities equally or by some firm-specific characteristic.

**풀이:** 지수 구성 시 대상 시장 정의(B), 가중 방식(C)은 반드시 결정해야 하지만, 명목 척도 vs. 구간 척도(A)는 지수 구성과 무관. 지수는 수치를 가져야 한다.
**정답: A**

---

다음 표를 사용하여 Q2~Q4에 답하시오:

| 주식 | 1월 1일 주가 | 1월 1일 발행 주식수(천) | 12월 31일 주가 | 12월 31일 발행 주식수(천) |
|------|------------|-------------------|--------------|-------------------|
| A | $22 | 1,500 | $28 | 1,500 |
| B | $40 | 10,000 | $50 | 10,000 |
| C | $34 | 3,000 | $30 | 3,000 |

**Q2.** 1년 수익률 (가격가중지수):

A. 12.5%.  B. 13.5%.  C. 18.0%.

**풀이:**

- 1월 1일: $(22 + 40 + 34) / 3 = 96 / 3 = 32$
- 12월 31일: $(28 + 50 + 30) / 3 = 108 / 3 = 36$
- 수익률: $(36 / 32) - 1 = 0.125 = 12.5\%$

**정답: A**

---

**Q3.** 1년 수익률 (동일가중지수):

A. 12.0%.  B. 12.5%.  C. 13.5%.

**풀이:**

- A 수익률: $(28 - 22) / 22 = 27.27\%$
- B 수익률: $(50 - 40) / 40 = 25.00\%$
- C 수익률: $(30 - 34) / 34 = -11.76\%$
- 평균: $(27.27\% + 25.00\% + (-11.76\%)) / 3 = 40.51\% / 3 = 13.5\%$

**정답: C**

---

**Q4.** 1년 수익률 (시가총액가중지수):

A. 12.5%.  B. 13.5%.  C. 18.0%.

**풀이:**

- 1월 1일 총 시가총액: $22 \times 1{,}500 + 40 \times 10{,}000 + 34 \times 3{,}000 = 33{,}000 + 400{,}000 + 102{,}000 = 535{,}000$ (천 달러)
- 12월 31일 총 시가총액: $28 \times 1{,}500 + 50 \times 10{,}000 + 30 \times 3{,}000 = 42{,}000 + 500{,}000 + 90{,}000 = 632{,}000$ (천 달러)
- 수익률: $(632{,}000 / 535{,}000) - 1 = 0.1813 = 18.1\% \approx 18.0\%$

**정답: C**

---

**Q5.** Market float of a stock is best described as its:

A. total outstanding shares.
B. shares that are available to domestic investors.
C. outstanding shares, excluding those held by controlling shareholders.

**풀이:** 시장 유동주식수(market float) = 전체 발행 주식에서 지배주주 보유분 제외한 실제 투자 가능 주식.
**정답: C**

---

**Q6.** For which of the following indexes will rebalancing occur most frequently?

A. A price-weighted index.
B. An equal-weighted index.
C. A market capitalization-weighted index.

**풀이:** 동일가중지수는 가격 변동 후 동일 비중이 깨지므로 주기적 리밸런싱 필요. 가격가중·시가총액가중은 가격 변동 자체가 비중 조정 역할 수행.
**정답: B**

---

## Module 40.2 지수의 용도와 유형

---

## LOS 40.f: 지수 리밸런싱과 재구성 (Describe rebalancing and reconstitution of an index)

### 리밸런싱 (Rebalancing)

- **정의:** 가격 변동으로 비중이 바뀐 후 목표 비중으로 되돌리는 작업
- 주로 **동일가중지수**에서 중요 (가격가중·시가총액가중은 가격 변동이 자동 조정)
- 통상 **분기별(quarterly)**로 실시

### 재구성 (Reconstitution)

- **정의:** 지수 구성 종목을 변경하는 것
- 이유: 상장폐지, 파산, 기준 미충족 등
- 편입 종목은 가격 **상승** 경향 (인덱스 펀드 매수 수요), 제외 종목은 **하락** 경향

---

## LOS 40.g: 증권시장 지수의 용도 (Describe uses of security market indexes)

### 5가지 주요 용도

| 용도 | 설명 | 주의사항 |
|------|------|---------|
| **시장 심리 반영** | 대표적 시장 수익률 → 투자자 신뢰 반영 | DJIA는 30개 종목만 포함, 광의 시장 대표성 제한 |
| **운용자 성과 벤치마크** | 액티브 매니저 성과 평가 기준 | 매니저 스타일과 일치하는 벤치마크 사용 (예: 가치주 매니저 → 가치 지수) |
| **시장 수익률·위험 측정** | 자산 배분의 기대 수익률·표준편차 추정 | 과거 지수 수익률 활용 |
| **베타·위험조정 수익률 측정** | CAPM에서 시장 포트폴리오 수익률 대용 | 베타 추정 및 기대 수익률 계산에 활용 |
| **인덱스 펀드 모델 포트폴리오** | 패시브 투자자의 지수 복제 | 인덱스 뮤추얼펀드, ETF, 사모 포트폴리오 |

---

## LOS 40.h: 주식 지수의 유형 (Describe types of equity indexes)

### 주식 지수 분류

| 지수 유형 | 특징 | 예시 |
|-----------|------|------|
| **광의 시장 지수(Broad market)** | 시장 전체의 90% 이상 포함 | Wilshire 5000 (6,000개 이상 종목) |
| **다국가 지수(Multi-market)** | 여러 국가 지수 결합, 지역·발전단계별 측정 | MSCI World, 신흥시장 지수 |
| **기본적가중 다국가 지수** | 국가 지수는 시가총액가중, 국가 간 비중은 펀더멘털(GDP 등) 기준 | — |
| **섹터 지수(Sector)** | 특정 산업 섹터 수익률 측정 | 헬스케어, 금융, 소비재 지수 |
| **스타일 지수(Style)** | 시가총액 + 가치/성장 전략 수익률 측정 | 소형 가치주 지수 |

**스타일 지수의 특징:**
- 소형/중형/대형주 기준: 절대 시가총액 또는 상대적 정의 (예: 최대 500개 = 대형주)
- 가치주/성장주 구분: PER, 배당수익률 등 활용
- 구성 종목의 **분류 이동(migration)** 빈번 → 광의 시장 지수보다 **편입 종목 교체율 높음**

---

## LOS 40.i: 증권시장 지수 유형 비교 (Compare types of security market indexes)

### 주요 글로벌 지수 비교표

| 지수명 | 대상 시장 | 구성 종목 수 | 가중 방식 | 특이사항 |
|--------|---------|------------|---------|---------|
| Dow Jones Industrial Average | 미국 대형주 | 30 | 가격가중 | WSJ 편집자 선정 |
| Nikkei Stock Average | 일본 대형주 | 225 | 수정 가격가중 | 고가 주식 조정 |
| TOPIX | 도쿄증권거래소 1부 전체 | 변동 | 유동주식수조정 시가총액가중 | 일본 주식 시가총액의 93% |
| MSCI All Country World Index | 23개 선진국 + 24개 신흥국 | 변동 | 유동주식수조정 시가총액가중 | 달러·현지통화 기준 모두 제공 |
| S&P 500 | 미국 대형주 500개 | 약 500 | 시가총액가중 | 기관투자가 표준 벤치마크 |
| S&P Developed Global Ex-U.S. BMI Energy Sector Index | 미국 외 선진국 에너지주 | 변동 | 유동주식수조정 시가총액가중 | ETF 모델 포트폴리오 |
| Barclays Capital Global Aggregate Bond Index | 글로벌 투자등급 채권 | 변동 | 시가총액가중 | 구 Lehman Brothers 편제 |
| Markit iBoxx Euro High-Yield Bond Indexes | 고수익 채권 | 변동 | 시가총액가중 | 월별 재구성 |
| FTSE EPRA/NAREIT Global Real Estate Index | 글로벌 부동산 | 변동 | 유동주식수조정 시가총액가중 | 공개 거래 REIT |
| HFRX Global Hedge Fund Index | 글로벌 헤지펀드 | 변동 | 자산가중 | 다양한 헤지펀드 전략 포함 |
| HFRX Equal Weighted Strategies EUR Index | 글로벌 헤지펀드 | 변동 | 동일가중 | HFRX Global과 동일 펀드 구성 |
| Morningstar Style Indexes | 미국 주식 (가치/성장 × 시가총액 3단계) | 변동 | 유동주식수조정 시가총액가중 | 9개 범주 |

**핵심 관찰:** 대부분의 주요 글로벌 지수는 **시가총액가중(유동주식수조정)** 방식 채택

---

## LOS 40.j: 채권 지수의 유형 (Describe types of fixed-income indexes)

### 채권 지수의 분류 기준

채권의 다양성으로 인해 다양한 분류 기준 존재:

| 분류 기준 | 예시 |
|-----------|------|
| 발행주체 | 정부, 정부기관, 기업 |
| 담보 종류 | 모기지, 자산담보부 |
| 쿠폰 | 고정금리, 변동금리 |
| 만기 | 단기, 중기, 장기 |
| 신용위험 | 투자등급 vs. 고수익(정크) |
| 인플레이션 보호 | TIPS 등 물가연동 |

### 채권 지수 구성의 어려움

| 문제점 | 설명 | 결과 |
|--------|------|------|
| **방대한 채권 유니버스** | 채권은 기업·정부·기관 모두 발행, 만기 되면 교체 필요 | 지수 회전율 높음 |
| **딜러 시장과 낮은 거래 빈도** | 채권은 주로 딜러 통해 거래, 가격 정보 딜러 의존 | 추정 가격 사용 필요 |
| **복제 어려움** | 방대한 종목 수, 높은 유동성 비용, 높은 회전율 | 채권 지수 복제 비용 高 |

---

## LOS 40.k: 대안투자 지수 (Describe indexes representing alternative investments)

### 1. 원자재 지수 (Commodity Indexes)

- 곡물, 축산물, 금속, 에너지 등의 **선물계약** 가격 기반
- 예: Thomson Reuters/Core Commodity CRB Index, S&P GSCI

**원자재 지수의 이슈:**

| 이슈 | 설명 |
|------|------|
| **가중 방식의 다양성** | 동일가중, 글로벌 생산량 가중, 고정 가중 등 다양 → 지수마다 위험·수익 특성 크게 상이 |
| **선물 vs. 현물** | 지수는 선물 가격 기반 (현물이 아님) → 위험없는 수익률 + 선물가격 변동 + **롤 수익률(roll yield)** 반영 → 실물 원자재 보유 수익률과 다를 수 있음 |

### 2. 부동산 지수 (Real Estate Indexes)

세 가지 구성 방식:

| 방식 | 특징 |
|------|------|
| **감정 기반(Appraisal)** | 부동산 감정 평가 기반 |
| **반복 매매(Repeat sales)** | 동일 부동산의 반복 거래 가격 기반 |
| **REIT 기반** | 공개 거래 REIT 주가 기반, 유동성 우수 |

REIT는 폐쇄형 뮤추얼펀드와 유사, 부동산·모기지 풀에 투자
FTSE International이 REIT 지수 가족 운영

### 3. 헤지펀드 지수 (Hedge Fund Indexes)

- 대부분 **동일가중** 방식
- 헤지펀드는 규제 받지 않고 성과 보고 의무 없음

**헤지펀드 지수의 문제:**

| 편향 유형 | 설명 |
|-----------|------|
| **자발적 보고 편향** | 좋은 펀드만 보고 → 수익률 상향 편향 |
| **생존 편향(Survivorship bias)** | 과거 보고했으나 성과 나빠진 펀드가 보고 중단 → 평균 수익률 상향 편향 |

→ **결론:** 헤지펀드 지수는 실제 헤지펀드 평균 수익률을 과대평가하는 경향

---

## Module Quiz 40.2

**Q1.** The publisher of an index removes three bonds nearing maturity and one that defaulted, and adds four actively traded bonds. This bond index is said to have been:

A. redefined.
B. rebalanced.
C. reconstituted.

**풀이:** 구성 종목의 추가·제거 = 재구성(reconstitution). 리밸런싱은 비중 조정.
**정답: C**

---

**Q2.** Which of the following would most likely represent an inappropriate use of an index?

A. As a reflection of market sentiment.
B. Comparing a small-cap manager against a broad market.
C. Using the CAPM to determine the expected return and beta.

**풀이:** 소형주 매니저를 광의 시장 지수와 비교하면 부적절. 벤치마크는 매니저 스타일과 일치해야 함.
**정답: B**

---

**Q3.** An index of 200 mid-cap growth stocks is best described as a:

A. style index.
B. sector index.
C. broad market index.

**풀이:** 중형 성장주 지수 = 시가총액(중형) + 스타일(성장) → 스타일 지수. 섹터 지수는 특정 산업.
**정답: A**

---

**Q4.** Which of the following is least accurate regarding fixed-income indexes?

A. Replicating the return on a fixed-income security index is difficult for investors.
B. There is a great deal of heterogeneity in the composition of fixed-income security indexes.
C. Due to the large universe of fixed-income security issues, data for fixed-income securities are relatively easy to obtain.

**풀이:** 채권은 주로 딜러 시장에서 거래되고 거래 빈도가 낮아 가격 데이터 획득이 **어렵다**. C는 틀린 설명.
**정답: C**

---

**Q5.** Which of the following indexes of alternative investments is most likely to be calculated from derivatives prices?

A. Real estate index.
B. Commodity index.
C. Hedge fund index.

**풀이:** 원자재 지수는 원자재 **선물계약(futures)** 가격 기반.
**정답: B**

---

**Q6.** Most of the widely used global security indexes are:

A. price weighted.
B. equal weighted.
C. market capitalization weighted.

**풀이:** MSCI, FTSE, S&P 등 주요 글로벌 지수는 대부분 시가총액가중(유동주식수조정).
**정답: C**

---

## 핵심 개념 정리

### LOS 40.a 요약
- 지수 = 자산군·시장·시장 세그먼트 성과 측정 도구
- 구성 증권의 시장 가격 기반, 지수 수익률 = 지수값의 %변화

### LOS 40.b 요약
- **가격 수익률(Price return):** 가격 변동만 반영
- **총 수익률(Total return):** 가격 + 배당·이자 반영 (항상 ≥ 가격 수익률)

$$R_P = \prod_{k=1}^{K}(1 + R_{Sk}) - 1$$

### LOS 40.c 요약
- 지수 구성 결정 사항: 대상 시장, 편입 종목, 가중 방식, 리밸런싱 주기, 재구성 주기

### LOS 40.d 요약
- **가격가중:** 단순, 고가 주식 편향
- **동일가중:** 단순, 소형주 편향, 리밸런싱 필요
- **시가총액가중:** 집합 투자자 부의 변화 반영, 과대평가 주식 편향
- **유동주식수조정:** 실제 투자 가능 비중 반영
- **기본적 가중:** 펀더멘털 기반, 가치 편향

### LOS 40.e 요약

$$\text{가격가중지수} = \frac{\sum \text{주가}}{\text{조정된 제수(N)}}$$

$$\text{시가총액가중지수} = \frac{\text{현재 총시가총액}}{\text{기준기간 총시가총액}} \times \text{기준 지수값}$$

$$\text{동일가중지수 변화} = \frac{\sum \text{개별 수익률}}{N} \implies \text{새 지수} = \text{기존 지수} \times (1 + \text{평균 수익률})$$

### LOS 40.f 요약
- **리밸런싱:** 목표 비중 유지 (동일가중지수에서 가장 중요, 보통 분기별)
- **재구성:** 편입 종목 변경 (편입 → 가격 상승 경향, 제외 → 하락 경향)

### LOS 40.g 요약
- 5가지 용도: 시장 심리 반영, 벤치마크, 시장 위험·수익 측정, 베타 추정, 인덱스 펀드 기준

### LOS 40.h 요약
- 광의 시장, 다국가, 섹터, 스타일 지수
- 스타일 지수: 구성 종목 이동 빈번 → 회전율 高

### LOS 40.i 요약
- 글로벌 지수는 대부분 유동주식수조정 시가총액가중
- 지리, 섹터, 발전 단계, 펀더멘털 기준으로 분류

### LOS 40.j 요약
- 채권 지수: 방대한 유니버스, 딜러 가격 의존, 높은 회전율, 복제 어렵고 비용 큼

### LOS 40.k 요약
- 원자재 지수: 선물 기반, 가중 방식 다양 → 지수 간 성과 크게 상이
- 부동산 지수: 감정·반복매매·REIT 기반
- 헤지펀드 지수: 자발적 보고 → 상향 편향 (생존 편향)

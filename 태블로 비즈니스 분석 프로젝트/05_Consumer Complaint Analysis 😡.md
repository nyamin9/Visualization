# 😡 Consumer Complaint Analysis (📆 2023.03.27 ~ 2023.03.31)  

<br>  


## 😡 1. 비즈니스 시나리오 정의  

<br>  

Vizable USA Financial 사의 분석팀으로서, consumer의 complaint 데이터를 분석하여 회사의 임원진이 취할 Action을 도울 수 있는 대시보드를 제작할 것입니다. 본사에 대한 소비자들의 불만을 tracking하고 인사이트를 도출하기 위해서, 기업 Product의 연도별 KPI를 사용합니다. 사용한 KPI의 종류는 아래와 같습니다.  

<br>  

 

 

(1) complaint count : 년도별 총 complain의 수를 의미합니다.  


 

(2) monetary relief rate : 회사 측이 금전적인 보상을 통해 해결한 complaint의 비율을 의미합니다.  


 

(3) disputed rate : 전체 complaint 중에서 complaint가 항의로 구성되거나, 갈등 이후에 해결되는 비율입니다.  
 
<br>  

각 KPI를 통해 complaint의 규모와 회사의 수익성, 회사의 인식에 영향을 주는 요인들을 파악하고자 합니다.  

<br>  

***  

<br>  

## 😡 2. 대시보드 설명  

<br>  

![img1 daumcdn](https://user-images.githubusercontent.com/65170165/236702135-471e7ac3-a1b5-4206-8bbc-ce7b4a7ca891.png)  

<br>  


☑️ 필터 : 각 년도별 Product에 대한 KPI를 파악하기 위해 [년도, Product] 두 가지 필터를 사용했습니다.  


 

☑️ 라인차트 : 각 년도의 월별 complaint의 수와 disputed complaint의 추세를 나타냈습니다.  


 

☑️ 파이차트 : 필터 설정값에 대한 complaint에서 높은 비중을 차지하는 상위 3개의 issue를 나타냅니다.  


 

☑️ 테이블차트 : 필터 설정값에 대한 complaint에서 각각의 issue에 대해 monetary relief rate를 계산하였습니다.  

 

 

☑️ 막대차트 : 필터 설정값에 대한 complaint에서 각각의 issue에 대해 Disputed rate를 구해주었습니다.  

<br>  

 

 

또한 각 차트의 관심있는 issue를 클릭할 시 해당 issue 부분이 하이라이트되도록 설정해주었습니다. 가장 상위에는 년도별 KPI를 요약하여 나타냄으로써 기업의 소비자 대응방식을 한눈에 볼 수 있게끔 구현하였습니다. 요약된 각 KPI 수치에 마우스오버할 경우, 전체 년도와 전체 Product에 대한 KPI가 테이블 형식으로 나오도록 설정하여 당해 수치와 전체 수치를 비교할 수 있도록 하였습니다.  

<br>  

***  

<br>  

## 😡 3. 대시보드 활용방안  

<br>  


 

2012년도 Credit Card에 대한 complaint response 분석 상황을 가정하였습니다.  

<br>  

![img1 daumcdn](https://user-images.githubusercontent.com/65170165/236702214-5e18378d-ce21-4e02-996b-6f4387caa8cf.png)  

<br>  


(1) 전반적인 KPI 파악  


 

세부지표를 살펴보기에 앞서 2012년도 Credit Card에 대한 전반적인 수치 파악을 진행합니다. 한 해동안 Credit Card에 대해 consumer가 제출한 complaint는 총 3,036 건이었으며, 전체 Product에 대한 complaint 6,507 건에 대해서 절반 가량의 비중을 차지하였습니다. 평균 disputed rate는 17.1%로 2012년도 전체 Product의 평균 disputed rate인 10.5% 보다 상당 비율 높은 수치를 기록하였습니다. 또한 평균 monetary relief rate는 36.1%로 2012년도 전체 Product의 평균 monetary relief rate인 20.9%에 비해 굉장히 높은 차이를 기록하였습니다. 2012년의 complaint 수는 5월부터 7월에 이르기까지 평균값보다 굉장히 많았습니다. 이러한 까닭에 전체적으로 제기된 불만의 수가 전년도 대비 급증한 것으로 보입니다. 다행히도 8월 이후부터는 complaint의 수가 현저히 줄어든 것으로 볼 때, 적극적인 소비자 대응 전략이 잘 관리되고 있는 듯 합니다. 전체적인 complaint의 추세와 유사하게 disputed complaint의 추세도 유지되고 있습니다.  

<br>  

 

 

(2) 주요 issue 파악  


 

Credit Card에 대해서 가장 많은 불만이 접수된 issue는 441건의 Billing disputes로 나타났습니다. 신용카드 제품에 대해 청구에 대한 complaint가 가장 많다는 것은 어떻게 보면 당연한 일이겠지만, 잘못 청구되는 경우 이는 곧바로 기업의 수익성에 영향을 줄 수 있으므로 적절한 대처가 필요합니다. 이를 판단하기 위해서는 해당 issue의 monetary relief rate를 파악하여 실수와 허수를 파악해야 할 듯 합니다.  



 

두번째로 많은 불만이 제기된 issue는 APR or interest rate 입니다. 신용카드의 연이율 혹은 금리에 대한 complaint가 제기되었다는 것을 의미합니다. 일반적으로 신용카드에 이율이 적용되는 경우는 카드대출 혹은 할부에 관한 내용일 것으므로, 이에 대한 금전적 보상은 만기 전에 대출을 상환하거나 할부 구매 상품을 환불하는 경우에 해당합니다. 해당 issue에 대해서는 대체적으로 consumer의 권리를 보장하는 법안이 마련되어 있기 때문에, 높은 monetary relief rate를 예측할 수 있을 것 같습니다.  


 

세번째 issue는 211건의 Identity theft / Fraud / Embezzlement 입니다. 앞선 두 issue에 비해서는 절반 정도의 비중을 차지하고 있습니다. 신원 도용에 관한 issue로써, 심각한 범죄입니다. 하지만 신원을 도용한 사람이 잡혀야 피해자의 신원이 보장되므로 피해 사실 입증이 어렵기 때문에, 낮은 monetary relief rate를 예측할 수 있습니다. 반면 피해를 본 consumer 입장에서는 굉장히 억울할 일이기 때문에, 높은 disputed complaint rate를 예상할 수 있을 듯 합니다.  


<br>  


 

(3) issue 별 금전적 대응 현황 파악  


 

이번에는 앞서 살펴본 상위 3개의 issue에 대한 monetary relief rate를 분석하겠습니다. 금전적 대응의 규모는 회사의 수익에 직접적인 영향을 줄 수 있기에 적절한 대응 방안이 필요할 것입니다. 가장 많은 비중을 차지한 Billing disputes는 47.8%, APR or interest rate 는 57.6%의 수치를, Identity theft / Fraud / Embezzlement는 20.9%를 기록하였습니다. 본 수치를 기반으로 확인했을 때, Billing disputes issue가 특히 눈에 띕니다. consumer가 사용하지 않은 내역에 대해 잘못 청구된 경우에 주로 complaint를 제기할 만한 상황에서, 절반에 가까운 불만에 대해 금전적으로 보상을 해주는 대응을 했다는 것은 200여건이 넘는 결제에 대해 잘못된 청구서를 요구했다는 의미입니다. 이는 소비자에 대한 제품의 신뢰 문제와 직결될 수 있기에, 해당 issue의 해당 수치에 대해 지속적인 Tracking이 요구됩니다.  


 

또한, APR or interest rate issue 역시 높은 비율을 보여줍니다. 하지만 전체 사용량 중 극히 일부인 complaint을 반영해 이자율이나 APR을 조정했다가는 전반적인 기업 수익성에 피해를 줄 수 있기에 섣부른 판단은 금해야 합니다. 이에 대해 대응책으로, 카드 상품의 이자율을 기간에 따라 세분화하는 방안을 제안합니다. 할부 기간을 조정하기는 어렵겠지만, 대출상품의 경우 기간과 이자율을 조정해 고객의 상황에 맞는 상품을 만들 수 있을 것입니다. 만기가 긴 상품의 경우 이자율을 늘리고, 짧은 상품의 경우 대출 금액과 이자율을 낮춰 다양한 배경의 consumer 유입을 유도하고, 나아가 높은 monetary relief rate의 해결을 기대할 수 있을 것으로 예상합니다.  

<br>  

 

 

(4) issue 별 고객 항의 현황 파악  


 

consumer가 항의한 complaint의 비율을 파악하기 위해서, disputed rate를 계산하였습니다. 소비자의 입장에서는 회사와의 컨택이 이뤄어지는 셈이기 때문에, 이에 대한 회사의 대응은 기업의 인식에 영향을 줄 것입니다. 앞서 예상했던 대로, 신원 도용에 해당하는 Identity theft / Fraud / Embezzlement issue의 경우 평균 17.1%를 상회하는 23.2%를 기록하면서 주요 3개 issue 중에서 가장 높은 값을 기록했습니다. 한편 나머지 두 issue에 대해서는 눈에 띌 만한 항의가 기록되지 않았습니다. consumer가 고압적인 태도를 취하지 않아도 이뤄지는 금전적 대응은 consumer에게 기업이 적절한 대응을 하고 있다는 인식을 만들어 줄 수 있기 때문에 지속적인 고객 유지가 가능한 이유가 될 수 있을 것입니다.  


 

전체 년도 기준으로 보았을 때 monetary relief rate가 이상치 수준으로 높은 해였지만, 오히려 disputed rate는 다른 년도에 비해서 낮은 수치를 기록하였습니다. 월별 complaint의 추세로 보아 상당히 많은 이슈와 불만을 산 한 해였음에도 불구하고, 소비자 대응 전략은 상당히 탁월했던 것으로 보입니다. 향후 회사의 제품에 대해서 많은 불만사항이 제기되는 상황에도, 2012년 Credit card 품목에 사용했던 전략에 3가지 KPI를 반영한다면 더욱 좋은 고객 대응 방식을 구현할 수 있을 것입니다.  

<br>  

***  

<br>  

## 😡 4. 프로젝트 진행 중 의문점 정리  

<br>  

Q1. 추세를 알아보기 위해 라인 차트를 만들긴 했지만, 전체 complaint와 disputed complaint를 비교하는 느낌으로도 표현하고 싶어서 막대차트를 사용할지 말지도 고민했습니다. 라인차트와 막대차트 중 어떤 차트가 좀 더 가독성있고, 제 의도가 잘 전달될지 궁금합니다.  

<br>  

 

 

Q2. 원래 submited date 필드를 바탕으로 달력 시트를 만들려고 했지만, 2001년부터 2020년 10월까지 모든 날짜가 있는 데이터가 아니기 때문에 새로운 날짜 엑셀 파일을 하나 만들어 complaint 데이터와 오른쪽 조인하여 구현하려 했습니다. 하지만 새롭게 만든 날짜 파일에는 Product에 대한 데이터가 Null값으로 지정되어 있어서 필터 지정 시 값이 없는 나머지 날짜가 없어지는 경우가 생겼습니다. 제 생각에는 조인을 하더라도 교집합 부분에 대해 중복을 허용한다면 모든 날짜에 대한 count 표시가 가능할 듯 한데, 어떻게 고칠 수 있을지 알려주시면 감사하겠습니다!!  

<br>  

***  

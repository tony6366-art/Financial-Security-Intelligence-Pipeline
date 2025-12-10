Financial Security Intelligence Pipeline

금융 보안 쪽 공부하면서 정리해 둔 실습용 파이프라인입니다.  
크게 보면 아래 네 단계로 나뉩니다.

1. 가상의 금융 거래 로그 생성
2. Spark 기반 이상 거래 탐지 (K-Means)
3. Threat Intelligence(IOC) 기반 위험 점수화
4. 최종 Fraud Score 계산 및 상위 위험 거래 리스트 출력

Spark 쪽은 예전에 만들었던 보안 로그 기반 이상 탐지 코드를 베이스로 했고,  
Threat Intel 쪽은 IOC 매칭 파이프라인을 조금 단순화해서 붙였습니다.

---

text
financial-security-intelligence-pipeline/
 ├── core/
 │    ├── finance_log_generator.py
 │    ├── spark_anomaly_detection.py
 │    ├── fraud_score_engine.py
 │    └── unified_pipeline.py
 ├── modules/
 │    ├── __init__.py
 │    └── threat_intel_fusion/
 │         ├── __init__.py
 │         ├── ti_data.py
 │         └── ti_engine.py
 ├── data/
 │    ├── synthetic_finance_logs.csv
 │    └── final_fraud_scored_logs.csv
 ├── notebooks/   (선택)
 │    └── colab_example.ipynb
 ├── requirements.txt
 └── README.md

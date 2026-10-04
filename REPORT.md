1. Tôi dùng AWS, us-east-1, EC2 (x86_64, n_jobs=2), source commit [SHA].
2. Dataset có 284.807 dòng (492 dòng fraud), chia train/validation/test 170.883 / 56.962 / 56.962 (tỉ lệ 60/20/20), seed 16.
3. Load dữ liệu mất 2,50 giây; training mất 3,50 giây; best iteration là 68.
4. AUC 0,9768, Accuracy 0,9995 (99,95%), F1 0,8478, Precision 0,9070, Recall 0,7959 trên tập test (decision threshold 0,5).
5. Latency 1 dòng 1,21 ms; throughput batch 1.000 dòng 308.986 dòng/giây; cách đo median, warm-up excluded, predict_proba on pandas input (50 lần lặp với 1 dòng, 10 lần lặp với batch 1.000 dòng).
6. CPU/RAM/Network tôi quan sát lúc 17:23 02/10/2026: ảnh đính kèm [monitor](monitor.png).
7. Billing tại 17:23: 0.88 USD
8. Tôi đã tải kết quả và xóa tài nguyên lúc 2026-10-02, 17:07:30.

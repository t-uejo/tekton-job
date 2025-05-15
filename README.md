# Tekton によるジョブ実行検証

## 検証におけるゴール

- Tekton Pipeline を使って、複数の job を実行させる。
- リターンコードから次のジョブを実行させるかを判定。
- Cronjob から Tekton Pipeline を実行させる。

## Tekton Pipeline のインストール

```bash
kubectl apply --filename https://storage.googleapis.com/tekton-releases/pipeline/latest/release.yaml
```

### 注意点

- release.yaml 適応時に TCS-ONE の web フィルターの影響で image を取得できないため、WiFi を社給スマホのテザリングに切り替え。（Google の公式なイメージから取得しているので問題なし）

## 参考記事

- [Getting started with Tasks | Tekton](https://qiita.com/sotoiwa/items/7ffd415185d2cbb9f1a1)
- [Tekton を Minikube で試す 1 #Docker - Qiita](https://tekton.dev/docs/getting-started/tasks/)

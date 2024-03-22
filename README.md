### やりたいこと
1. アプリのPRをマージすると、GitHub Actionsにより自動でイメージビルドが走ってcontainer registryにプッシュ
2. イメージの更新をargoCDが検知して、Kubernetesリポジトリにタグ更新コミットつきブランチを作成
3. GitHub Actionsでブランチ作成をトリガーにmainブランチ向けリリースPRを作成
4. mainブランチ向けリリースPRをマージすると、argoCDによりクラスターに適用

![cicd drawio](https://github.com/ta8i2chi8/sample-app-for-cicd-manifests/assets/66934929/3ab561dc-7e68-40a0-904d-b8b7b87a8842)

### 以下を参考に実装
https://techblog.zozo.com/entry/measure-argocd-introduction

---
title: 仮想マシン
status: Completed
category: テクノロジー
tags: ["基礎", "インフラストラクチャ", ""]
---

仮想マシン（VM）とは、特定のハードウェアに縛られないコンピューターとそのオペレーティングシステムのことです。
VMは、1台の物理コンピューターを複数の仮想コンピューターに分割する[仮想化](/ja/virtualization/)に依存しています。
この分割は、組織やインフラプロバイダーに、下層のハードウェアに影響を与えることなく、VMを簡単に作成、破棄することを可能にします。

## 解決すべき問題はなんですか

仮想マシンは仮想化を利用しています。[ベアメタル](/ja/bare-metal-machine/)マシンは単一のオペレーティングシステムに縛られているので、マシンのリソースをどれだけ使えるかはある程度制限されます。また、オペレーティングシステムも単一の物理マシンに縛られているので、その可用性はハードウェアに直結します。
物理マシンがメンテナンスやハードウェア故障によりオフラインになると、オペレーティングシステムもオフラインになります。

## どのように役に立つのでしょうか

オペレーティングシステムと物理マシンとの直接的な関係を取り除くことで、プロビジョニングの時間やハードウェア利用率、弾力性といったベアメタルマシンが抱えるいくつかの問題を解決することができます。

新しいハードウェアの購入やインストール、あるいはそれをサポートするための設定が必要ないため、新しいコンピューターのプロビジョニングの時間が劇的に短縮されます。
VMは、1台の物理マシン上に複数の仮想マシンを配置することで、既存の物理ハードウェアリソースをより有効に活用できます。
特定の物理マシンに縛られないため、VMは物理マシンよりも耐障害性に優れています。
物理マシンがオフラインになる必要がある場合、その上で稼働しているVMを、ほとんどない、あるいは全く停止時間なしで別のマシンに移動させることができます。

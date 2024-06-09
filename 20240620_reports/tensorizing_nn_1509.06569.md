# TensorNetwork for Machine Learning

論文: [https://arxiv.org/abs/1509.06569](https://arxiv.org/abs/1509.06569) [22 Sep 2015]


（まとめ @derwind）

- 著者
    - Alexander Novikov ${}^{1,4} Dmitry Podoprikhin ${}^1$ Anton Osokin ${}^2$ Dmitry Vetrov ${}^{1,3}$
- 所属
    - ${}^1$ Skolkovo Institute of Science and Technology, Moscow, Russia
    - ${}^2$ INRIA, SIERRA project-team, Paris, France
    - ${}^3$ National Research University Higher School of Economics, Moscow, Russia
    - ${}^4$ Institute of Numerical Mathematics of the Russian Academy of Sciences, Moscow, Russia

## どんなもの？

- ディープニューラルネットワーク（DNN）は多くの分野で最先端の性能を発揮する一方で、計算リソースを大量に消費
- 特に、一般的に使用される全結合層には大量のメモリが必要
- 全結合層の重み行列を Tensor Train フォーマットに変換することで、パラメータ数を大幅に削減 + 同時に層の表現力を維持
- VGG のネットワーク全体のサイズを 1/7 まで圧縮

## 先行研究と比べてどこがすごい？

**既存手法**

- 低ランク近似 (e.g., $W = AB$; $W \in \operatorname{Mat}(m,n)$ 行列（パラメータ数: $mn$）を $A \in \operatorname{Mat}(m,r)$ と $B \in \operatorname{Mat}(r,n)$ （パラメータ数: $r (m + n)$）に分解 / SVD: $W = U \Sigma V^\dagger$)

- ハッシュ技術: 全結合層の要素 $\{ a_{ij} \}$ をハッシュ関数でグループ化して、グループごとに値を共有する（重み共有）

**本研究**

- 低ランクのアイデアを一般化

## 技術や手法の肝は？

## どうやって有効だと検証した？

## 議論はある？

## 次に読むべき論文は？

- _CompactifAI: Extreme Compression of Large Language Models using Quantum-Inspired Tensor Networks_: https://arxiv.org/abs/2401.14109

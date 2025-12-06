# TreeQ: Pushing the Quantization Boundary of Diffusion Transformer via
Tree-Structured Mixed-Precision Search
[Kaicheng Yang](https://github.com/racoonykc), [Kaisen Yang](https://github.com/yks23),[Baiting Wu](https://github.com/1132213),[Xun Zhang](https://github.com/xun04),[Qianrui Yang](https://github.com/yangqianrui),[Haotong Qin](https://github.com/htqin), [He Zhang](https://github.com/hezhangsprinter),and [Yulun Zhang](https://github.com/yulunzhang).
[[arXiv]()] [[supplementary material](https://release-assets.githubusercontent.com/github-production-release-asset/1111003492/7955e824-937e-4e87-839f-e1a0bc60a615?sp=r&sv=2018-11-09&sr=b&spr=https&se=2025-12-06T05%3A35%3A48Z&rscd=attachment%3B+filename%3DSupp.pdf&rsct=application%2Foctet-stream&skoid=96c2d410-5711-43a1-aedd-ab1947aa7ab0&sktid=398a6654-997b-47e9-b12b-9515b896b4de&skt=2025-12-06T04%3A34%3A55Z&ske=2025-12-06T05%3A35%3A48Z&sks=b&skv=2018-11-09&sig=l7fZa5YmKFvt%2BgCG0FVTLRfB6SeeWkZ8MzgoweNyGDc%3D&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmVsZWFzZS1hc3NldHMuZ2l0aHVidXNlcmNvbnRlbnQuY29tIiwia2V5Ijoia2V5MSIsImV4cCI6MTc2NDk5Njc0NywibmJmIjoxNzY0OTk2NDQ3LCJwYXRoIjoicmVsZWFzZWFzc2V0cHJvZHVjdGlvbi5ibG9iLmNvcmUud2luZG93cy5uZXQifQ.Joy08YDIxhEU9vgT-s4TaQlAhUlbOo4ZfWDtmJjyjaA&response-content-disposition=attachment%3B%20filename%3DSupp.pdf&response-content-type=application%2Foctet-stream)] 

#### 🔥🔥🔥 News

- **2025-12-06:** Repository initial release.

---

> **Abstract:** Diffusion Transformers (DiTs) have emerged as a highly scalable and effective backbone for image generation, outperforming U-Net architectures in both scalability and performance. However, their real-world deployment remains challenging due to high computational and memory demands. Mixed-Precision Quantization (MPQ), designed to push the limits of quantization, has demonstrated remarkable success in advancing U-Net quantization to sub-4-bit settings while significantly reducing computational and memory overhead. Nevertheless, its application to DiT architectures remains limited and underexplored. In this work, we propose *TreeQ*, a unified framework addressing key challenges in DiT quantization. First, to tackle inefficient search and proxy misalignment, we introduce *Tree-Structured Search (TSS)*. This DiT-specific approach leverages the architecture's linear properties to traverse the solution space in $\mathcal{O(n)}$ time while improving objective accuracy through comparison-based pruning. Second, to unify optimization objectives, we propose *Environmental Noise Guidance (ENG)*, which aligns Post-Training Quantization (PTQ) and Quantization-Aware Training (QAT) configurations using a single hyperparameter. Third, to mitigate information bottlenecks in ultra-low-bit regimes, we design the *General Monarch Branch (GMB)*. This structured sparse branch prevents irreversible information loss, enabling finer detail generation. Through extensive experiments, our *TreeQ* framework demonstrates state-of-the-art performance on DiT-XL/2 under W3A3 and W4A4 PTQ/PEFT settings. Notably, our work is the first to achieve near-lossless 4-bit PTQ performance on DiT models.
---

### Visualization



![Visual comparison on DiT-XL/2 under low-bit PTQ](figs/visual_compare.png)

*Fig1:TreeQ(right) achieves better generation compared to baseline(left) under low-bit PTQ on DiT-XL/2*

![Visualization comparison between TSS and traditional methods Integer Programming. ](figs/treesearch.png)

*Fig2:Visualization comparison between TSS(right) and traditional methods Integer Programming(left).*



![GMB provides more details for low-bit quantized DiT4SR (left) and FLUX-Schnell (right), advancing practical applications.](figs/GMB_compare.png)

*Fig3:GMB provides more details for low-bit quantized DiT4SR (left) and FLUX-Schnell (right), advancing practical applications.*

## 🔖 TODO


- [ ] Release ckpt,training and inference code
- [ ] Release inference engine
- [ ] Release more quantized DiTs

---

## 💡 Acknowledgements

This code is built on [Diffusion Transformer](https://github.com/facebookresearch/DiT).
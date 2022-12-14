---
date created: 2022-10-20
date modified: 2022-10-24
title: NLD
---

NLD (Nonlinear devices)是一种利用失真（harmonics distortion and intermodulation distortion）现象，让人可以听到缺失频率的声音的方法。  
VSB在时域上构建谐波的常见算法。特点是：

1. **内存占用小**
2. **实时运算**

#### [[@Adam J Hill]],[[@Adam Hill, Malcolm Hawksford  2010]]在论文中指出

1. 相比PV, NLD performs particularly well for **transient heavy musical signals** such as **drum beats, staccato cello and double-bass，以及一些老歌 ** . 但是不适合vocals or organ。
2. 但是NLD的缺点是只通过HPF/BPF， approximate control the frequency components, 而无法针对调制失真 (intermodulation distortion)进行处理，而调制失真对造成声音的不自然。

#### [[@Woon-Seng Gan, Nay Oo  2008]] 对不同类别的NLD generator 进行对比测试后，认为The harmonic components NLD is the best for VBS：

1. **FWR 和 HWR 会造成perceived pitch is one octave higher thatn the orignal pitch**
- Full-wave rectifier (FWR)， 早期NLD使用，缺点是只能构建偶数倍谐波
- Half Wave Rectifier (HWR), 只能构建 fundamental 和 even harmonics，相比FWR多一个fundamental
2. **The hard limiter 和 square-wave 只能构建奇数倍的harmonics，且无法构建fundamental。 同样的在听感上会提升一个octave的pitch**
3. **The harmonic components** generated by the exponential NLD have both even and odd ordered components, including fundamental component. 此外，The harmonic components 还有一个参数b，可以调节harmonics 的richness，

#### [[@Eloi Moliner]]

1. NLD shows poor performance in intermodulation distortion tests. However, since we are applying this NLD to transient signals, which are non-tonal, intermodulation distortion can be neglected.

#### [[@Nay Oo, Malcolm Hawksford  2011]] 做了大量实验选择对VBS最好的NLD，把distortion 分为两类

**1. desirable distortion**
- can create the sensation of a warmer, richer and pleasing sound quality by subjectively extending the low-frequencies bandwidth
**1. undesirable distortion**
- induces perceptually unpleasant and discordant artifacts.
![[Screen Shot 2022-10-24 at 10.22.09.png]]



对于gain的选择，a weighting 对低频的降幅太多，不适合当前音乐的特性，所以选择k weighting

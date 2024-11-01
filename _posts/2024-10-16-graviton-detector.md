---

layout: post  
title: "Can we ever detect the graviton?"  
categories: physics

---

A graviton $G$ is a theoretical **quantum** of the gravitational field, which presumably exists if gravity can indeed be quantized. There remains an important question regarding this fundamental particle: Can we ever detect a single graviton?

Sadly, the answer is almost certainly not. This question occupied renowned physicist **Freeman Dyson** for some time, which puts us in good company. Let us explore some of the reasons why graviton detection is so elusive.

_The following is based in part on:_

- Rothman, T., and S. Boughn. "Can gravitons be detected?" _Foundations of Physics_ **36** (2006): 1801–1825. [10.1007/s10701-006-9081-9](https://doi.org/10.1007/s10701-006-9081-9) [arXiv:gr-qc/0601043](https://arxiv.org/abs/gr-qc/0601043)

- Dyson, F. "Is a graviton detectable?" _International Journal of Modern Physics A_ **28.25** (2013): 1330041. [10.1142/S0217751X1330041X](https://doi.org/10.1142/S0217751X1330041X)

## Compton scattering

To demonstrate why the graviton is so difficult to measure, let's first look at the Compton scattering differential cross-section $d\sigma/d\Omega$. This involves the scattering of a photon $\gamma$ off an electron $e^{-}$ given by

$$
\gamma(\lambda) + e^{-}(p) \rightarrow \gamma(\lambda') + e^{-}(p'),
$$

where $\lambda$ is the photon's wavelength and $p$ is the electron's momentum. The final wavelength and momentum after scattering are denoted by primes. The likelihood of scattering is given by the Klein-Nishina formula

$$
\frac{d\sigma}{d\Omega} = \frac{\alpha^{2}\hbar^{2}}{2m_{e}^{2}c^{2}}\left(\frac{\lambda}{\lambda'}\right)^{2}\left(\frac{\lambda}{\lambda'}+\frac{\lambda'}{\lambda}-\sin^{2}\theta\right).
$$

This is a rather daunting formula (and a "fun" derivation to accomplish for any physics graduate student in QED), but the important aspect I want to focus on is the coefficient out front, which depends on the ratio

$$
\frac{d\sigma}{d\Omega} \sim \frac{\alpha^{2}\hbar^{2}}{2m_{e}^{2}c^{2}} \sim 10^{-26}\ \mathrm{cm}^{2},
$$

which is proportional to the fine-structure constant squared, $\alpha^{2} \approx \left( \frac{1}{137} \right)^{2}$, divided by the square of the electron mass. Compton scattering is regularly measured and observed. Therefore, a cross-section on the order of $10^{-26}\ \mathrm{cm}^{2}$ is measurable by a careful undergraduate physicist.

## Gravito-Compton scattering

Let's now turn our attention to the scattering of a graviton off an electron (i.e., gravito-Compton scattering), which looks like

$$
G(\lambda) + e^{-}(p) \rightarrow G(\lambda') + e^{-}(p').
$$

By dimensional analysis, the cross-section from a scattering event of a graviton and an electron scales as

$$
\frac{d\sigma}{d\Omega} \sim \frac{G_{N}^{2}m_{e}^{2}}{c^{4}} \sim 10^{-111}\ \mathrm{cm}^{2}.
$$

In other words, the likelihood of a graviton scattering event is reduced compared to the scattering of photons by a factor of

$$
\frac{d\sigma_\mathrm{photon}}{d\sigma_\mathrm{graviton}} \sim 10^{85},
$$

which is a rather astonishing reduction! To some extent, we should not be surprised. Every undergraduate physicist is taught that gravity is a much weaker force than any of the other fundamental interactions in nature. Regardless, seeing these ratios explicitly is sobering. For a more detailed analysis, I point the reader to:

- Gross, D. J., and R. Jackiw. "Low-energy theorem for graviton scattering." _Physical Review_ **166.5** (1968): 1287. [10.1103/PhysRev.166.1287](https://doi.org/10.1103/PhysRev.166.1287)

## Electrogravitational conversion

The ratio $10^{85}$ of electromagnetic-to-gravitational scattering might seem insurmountable, but there is another process that has a much higher cross-section. This process is called "electrogravitational conversion," which is the transmutation of a graviton into a photon via collision with an electron. Schematically we write

$$
G(\lambda) + e^{-}(p) \rightarrow \gamma(\lambda') + e^{-}(p').
$$

Again, we appeal to dimensional analysis to obtain the scale of this process. This yields

$$
\frac{d\sigma}{d\Omega} \sim \frac{\alpha^{2}G_{N}\hbar}{c^{3}} \sim 10^{-70}\ \mathrm{cm}^{2},
$$

which is certainly an improvement over the gravito-Compton result by a factor of $10^{41}$. But this still leaves us with a process dramatically weaker than electromagnetic interactions, putting it well out of reach of any realistic experiment. For a full analysis of electrogravitational conversion, I refer the reader to:

- De Logi, W. K., and A. R. Mickelson. "Electrogravitational conversion cross sections in static electromagnetic fields." _Physical Review D_ **16.10** (1977): 2915. [10.1103/PhysRevD.16.2915](https://doi.org/10.1103/PhysRevD.16.2915)

## Planetary sized graviton detectors

Regardless of the challenges of detecting the graviton today, we can imagine a far future where humanity uses highly advanced technology to attempt to detect gravitons. To do this, these future scientists would need to build planetary sized detectors to even have a shred of hope. Let me quote an amusing excerpt from Dyson's paper:

> "If we imagine the whole mass of the Earth to be available as raw material for the manufacture of graviton detectors, with the cross-section (21) per electron and the flux (24), the counting rate is $2.4 \times 10^{-17}$ per second. If the experiment continues for the lifetime of the Sun, which is 5 billion years, the expected total number of gravitons detected will be 4. The experiment barely succeeds, but in principle, it can detect gravitons."

Even if future humanity attempts such a feat, there are further difficulties that oppose conclusive graviton detection. In an ironic twist, the main difficulty (neglecting the challenges of a 5-billion-year experimental runtime) is that even if you could build a fantastical detector the size of a planet, your signal would be virtually impossible to separate from the neutrino background, a famously weakly interacting particle. Quoting Rothman and Boughn:

> "A shield should be thicker than the mean-free-path for neutrinos, which for materials of ordinary density amounts to light years. Such a shield would collapse into a black hole. Unless one can find another way to discriminate against neutrinos, this appears to make detection of thermal gravitons impossible."

Rothman and Boughn's prognosis is also pretty clear:

> "Certainly, if a 'no graviton' law appears elusive, we do feel entitled to predict that no one will ever detect one in our universe."

Despite the finality of that sentiment, work on this problem continues, and you can find a more recent analysis from the perspective of optics here:

- Carney, D., V. Domcke, and N. L. Rodd. "Graviton detection and the quantization of gravity." _Physical Review D_ **109.4** (2024): 044009. [10.1103/PhysRevD.109.044009](https://doi.org/10.1103/PhysRevD.109.044009) [arXiv:2308.12988](https://arxiv.org/abs/2308.12988)

_Popular science article on the Carney et. al. proposal:_

- Wood, C. "It Might Be Possible to Detect Gravitons After All." _Quanta Magazine_ (10-30-2024). [https://www.quantamagazine.org/it-might-be-possible-to-detect-gravitons-after-all-20241030/](https://www.quantamagazine.org/it-might-be-possible-to-detect-gravitons-after-all-20241030/)


_Further discussion of this blog post can be found in this [reddit thread](https://www.reddit.com/r/Physics/comments/1g84j8l/can_we_ever_detect_the_graviton_no_but_how_come/) and [tildes post](https://tildes.net/~science/1jkz/can_we_ever_detect_the_graviton_no_but_why_not)._

---

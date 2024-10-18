---

layout: post  
title: "Can we ever detect the graviton?"  
categories: physics

---

A graviton $G$ is a theoretical quanta of the gravitational field which presumably exists if gravity can indeed be quantized. There remains an important question regarding this fundamental particle: Can we ever detect a single graviton?

Sadly, the answer is almost certainly not. This question is one which occupied renown physicist Freemann Dyson for some time which puts us in good company, so let us explore some of the reasons why graviton detection is so illusive.

_The following is based in part on:_

- Rothman, T., and Stephen B. "Can gravitons be detected?" *Foundations of Physics* **36** (2006): 1801–1825. [10.1007/s10701-006-9081-9](https://doi.org/10.1007/s10701-006-9081-9) [arXiv:gr-qc/0601043](https://arxiv.org/abs/gr-qc/0601043)

## Compton scattering

To demonstrate why the graviton is so difficult to measure, let's first look at the Compton scattering differential cross-section $d\sigma/d\Omega$ which involves the scattering of a photon $\gamma$ off an electron $e^{-}$

$$
\gamma(\lambda) + e^{-}(p) \rightarrow \gamma(\lambda') + e^{-}(p'),
$$

where $\lambda$ is photon's wavelength and $p$ the electron momentum. The final wavelength and momentum after scattering are denoted by primes. The likelihood of scattering is given by the Klein-Nishina formula

$$
\frac{d\sigma}{d\Omega} = \frac{\alpha^{2}\hbar^{2}}{2m_{e}^{2}c^{2}}\left(\frac{\lambda}{\lambda'}\right)^{2}\left(\frac{\lambda}{\lambda'}+\frac{\lambda'}{\lambda}-\sin^{2}\theta\right).
$$

This is a rather daunting formula (and a "fun" derivation to accomplish for any physics graduate student in QED), but the important aspect I want to focus on is the coefficient out front which depends on the ratio

$$
\frac{d\sigma}{d\Omega} \sim \frac{\alpha^{2}\hbar^{2}}{2m_{e}^{2}c^{2}} \sim 10^{-26}\ \mathrm{cm}^{2},
$$

which proportional to the fine-structure constant squared $\alpha^{2}\approx\left(\frac{1}{137}\right)^{2}$ divided by the square of the electron mass. Compton scattering is regularly measured and observed, therefore the cross-section characteristic magnitude of $10^{-26}\ \mathrm{cm}^{2}$ should be thought of as measurable by a careful undergraduate physicist.

## Gravito-Compton scattering

Let's now turn our attention to scattering by a graviton off an electron (i.e. gravito-Compton scattering) which looks like

$$
G(\lambda) + e^{-}(p) \rightarrow G(\lambda') + e^{-}(p').
$$

By dimensional analysis, the cross-section from a scattering event of a graviton and an electron goes as

$$
\frac{d\sigma}{d\Omega} \sim \frac{G_{N}^{2}m_{e}^{2}}{c^{4}} \sim 10^{-111}\ \mathrm{cm}^{2}.
$$

Or in otherwords, the likelihood of a graviton scattering event is reduced compared to the scattering of photons by a factor of

$$
\frac{d\sigma_\mathrm{photon}}{d\sigma_\mathrm{graviton}} \sim 10^{85}
$$

A rather astonishing reduction!

## Electrogravitational conversion

The ratio $10^{85}$ of electromagnetic-to-gravitational scattering might seem insurmountable, but there is another process which has a much higher cross-section. This process is called "electrogravitational conversion" which is the transmuting of a graviton into a photon via collision with an electron

$$
G(\lambda) + e^{-}(p) \rightarrow \gamma(\lambda') + e^{-}(p').
$$

Again, we appeal to dimensional analysis to obtain the scale of this process. This yields

$$
\frac{d\sigma}{d\Omega} \sim \frac{\alpha^{2}G_{N}\hbar}{c^{3}} \sim 10^{-70}\ \mathrm{cm}^{2},
$$

which is certainly an improvement over the gravito-Compton result by a factor of $10^{41}$. But this still leaves us with a process comically weaker than the electromagnetic interactions putting it well out of reach of any realistic experiment. For a full analysis of electrogravitational conversion, we refer the reader to:

- De Logi, Walter K., and Alan R. Mickelson. "Electrogravitational conversion cross sections in static electromagnetic fields." _Physical Review D_ **16.10** (1977): 2915. [10.1103/PhysRevD.16.2915](https://doi.org/10.1103/PhysRevD.16.2915)

## Plantary sized graviton detectors

Regardless of the challenges of detecting the graviton today, we can image a far future where humanity using highly advanced technology attempts to detect gravitons. To do this, these future scientists would need to build planetary sized detectors, say on the scale of the mass of Jupiter $M_\mathrm{Jupiter}$, to even have a shred of hope. Even if future humanity attempts such a feat, there's further difficulties which face conclusive graviton detection.

In an ironic twist: the main difficulty in detecting gravitons is that even if you could build a fantastical detector the size of Jupiter, your signal would be virtually impossible to separate from the neutrino background, a famously weakly interacting particle. Quoting Rothman and Stephen:

> "A shield should be thicker than the mean-free-path for neutrinos, which for materials of ordinary density amounts to light years. Such a shield would collapse into a black hole. Unless one can find another way to discriminate against neutrinos, this appears to make detection of thermal gravitons impossible."

Let me quote an amusing excerpt from Dyson's paper:

> "If we imagine the whole mass of the Earth to be available as raw material for the manufacture of graviton detectors, with the cross-section (21) per electron and the flux (24), the counting rate is \(2.4 \times 10^{-17}\) per second. If the experiment continues for the lifetime of the Sun, which is 5 billion years, the expected total number of gravitons detected will be 4. The experiment barely succeeds, but in principle, it can detect gravitons."

Rothman and Boughn's prognosis is pretty clear

> *"Certainly, if a 'no graviton' law appears elusive, we do feel entitled to predict that no one will ever detect one in our universe."*

And here's a recent paper tackling the issue from an optics perspective (though I haven't read it yet):

- Carney, Daniel, Valerie Domcke, and Nicholas L. Rodd. "Graviton detection and the quantization of gravity." arXiv preprint arXiv:2308.12988 (2023). [arXiv:2308.12988](https://arxiv.org/abs/2308.12988)

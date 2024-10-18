---

layout: post  
title: "Can we ever detect the graviton?"  
categories: physics

---

A graviton is a theoretical quanta of the gravitational field which presumably exists if gravity can indeed be quantized. There remains an important question regarding this fundamental particle: Can we ever detect a single graviton? Sadly, the answer is almost certainly not.

## Compton scattering

To demonstrate, let's look at the Compton scattering differential cross-section which involves the scattering of a photon $\gamma$ off an electron $e^{-}$

$$
\gamma(\lambda) + e^{-}(p) \rightarrow \gamma(\lambda') + e^{-}(p'),
$$

where $\lambda$ is photon's wavelength and $p$ the electron momentum. The final wavelength and momentum after scattering are denoted by primes. The likelihood of scattering is given by the Klein-Nishina formula

$$
\frac{d\sigma}{d\Omega} = \frac{\alpha^{2}\hbar^{2}}{2m_{e}^{2}c^{2}}\left(\frac{\lambda}{\lambda'}\right)^{2}\left(\frac{\lambda}{\lambda'}+\frac{\lambda'}{\lambda}-\sin^{2}\theta\right).
$$

This is a rather daunting formula (and a "fun" derivation to accomplish for any physics graduate student in QED) but the important aspect I want to focus on is the coefficient out front which depends on the ratio

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
\frac{d\sigma}{d\Omega} \sim \frac{G^{2}m_{e}^{2}}{c^{4}} \sim 10^{-111}\ \mathrm{cm}^{2}.
$$

Or in otherwords, the likelihood of a graviton scattering event is reduced compared to the scattering of photons by a factor of

$$
\frac{d\sigma_\mathrm{photon}}{d\sigma_\mathrm{graviton}} \sim 10^{85}
$$

A rather astonishing reduction! This might seem like all hope is lost, but there is another process which has a much higher cross-

Here's the relevant literature that addresses this question

- Rothman, Tony, and Stephen Boughn. "Can gravitons be detected?" *Foundations of Physics* **36** (2006): 1801–1825. [arXiv:gr-qc/0601043](https://arxiv.org/abs/gr-qc/0601043)

- Dyson, Freeman. "Is a graviton detectable?" *International Journal of Modern Physics A* **28**, no. 25 (2013): 1330041. [doi:10.1142/S0217751X1330041X](https://doi.org/10.1142/S0217751X1330041X)

There's an ironic twist: the main difficulty in detecting gravitons is that even if you could build a fantastical detector the size of Jupiter (as Dyson discusses), your signal would be virtually impossible to separate from the neutrino background—a famously weakly interacting particle.

Let me quote an amusing excerpt from Dyson's paper

> *"If we imagine the whole mass of the Earth to be available as raw material for the manufacture of graviton detectors, with the cross-section (21) per electron and the flux (24), the counting rate is \(2.4 \times 10^{-17}\) per second. If the experiment continues for the lifetime of the Sun, which is 5 billion years, the expected total number of gravitons detected will be 4. The experiment barely succeeds, but in principle, it can detect gravitons."*

Rothman and Boughn's prognosis is pretty clear

> *"Certainly, if a 'no graviton' law appears elusive, we do feel entitled to predict that no one will ever detect one in our universe."*

And here's a recent paper tackling the issue from an optics perspective (though I haven't read it yet):

- Carney, Daniel, Valerie Domcke, and Nicholas L. Rodd. "Graviton detection and the quantization of gravity." arXiv preprint arXiv:2308.12988 (2023). [arXiv:2308.12988](https://arxiv.org/abs/2308.12988)

---
date: 2025-04-26T17:58
tags:
  - Electrical
cssclasses:
  - center-titles
---
# Alternating Current

## Impedance and Reactance

$$
\begin{gathered}
Z = \frac{V_m}{I_m} = \frac{V_{rms}}{I_{rms}} \\ \\
X_L = \omega L \\ \\
X_C = \frac{1}{\omega C}
\end{gathered}
$$

## Simple AC Circuits

### AC Circuit with a Resistor only
$$
\begin{gathered}
i_o = \frac{\mathcal{E}}{R} \\ \\
i = i_o\sin\omega t \\ \\
\mathcal{E} = \mathcal{E}_o\sin\omega t
\end{gathered}
$$

### AC Circuit with a Capacitor only

$$
\begin{gathered}
i_o = C\mathcal{E}_o\ \omega \\ \\
i = i_o\sin(\omega t\ +\ \frac{\pi}{2}) \\ \\
\mathcal{E} = \mathcal{E}_o\sin\omega t
\end{gathered}
$$
> Current **leads** voltage by π/2 radians.

### AC Circuit with an Inductor only

$$
\begin{gathered}
i_o = \frac{\mathcal{E}_o}{\omega L} \\ \\
i = i_o\sin(\omega t\ -\ \frac{\pi}{2}) \\ \\
\mathcal{E} = \mathcal{E}_o\sin\omega t
\end{gathered}
$$
> Current **lags** voltage by π/2 radians.

## Impedance and Admittance
$$
\begin{gathered}
Z = \frac{\mathcal{E}_o}{i_o} \\ \\
Y = \frac{1}{Z} = \frac{i_o}{\mathcal{E}_o}
\end{gathered}
$$

## Complex AC Circuits

### RC Circuit

$$
\begin{gathered}
Z = \sqrt{R^2 + (\frac{1}{\omega C})^2}
\end{gathered}
$$

Peak current is defined as
$$
\begin{gathered}
i_o = \frac{\mathcal{E}_o}{Z} = \frac{\mathcal{E}_o}{\sqrt{R^2 + (\frac{1}{\omega C})^2}} \\ \\
\tan{\upvarphi} = \frac{1}{\omega \ CR}
\end{gathered}
$$

The steady-state current is
$$
i = \frac{\mathcal{E}_o}{Z}\sin(\omega t\ -\ \upvarphi)
$$

### RL Circuit


$$
\begin{gathered}
Z = \sqrt{R^2 + (\omega L)^2}
\end{gathered}
$$

Peak current is defined as
$$
\begin{gathered}
\tan{\upvarphi} = \frac{\omega L}{R}
\end{gathered}
$$

The steady-state current is
$$
i = \frac{\mathcal{E}_o}{Z}\sin(\omega t\ -\ \upvarphi)
$$

### LCR Circuit


$$
\begin{gathered}
X = X_C - X_L = (\frac{1}{\omega C} - \omega L)
\end{gathered}
$$
$$
\begin{gathered}
Z = \sqrt{R^2 + (\frac{1}{\omega C} - \omega L)^2} \\ \\
\tan{\upvarphi} = \frac{\frac{1}{\omega C} - \omega L}{R}
\end{gathered}
$$

The steady-state current is
$$
i = \frac{\mathcal{E}_o}{Z}\sin(\omega t\ -\ \upvarphi)
$$

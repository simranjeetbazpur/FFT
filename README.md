# Cooley Tukey FFT

<img src="http://www.alwayslearn.com/DFT%20and%20FFT%20Tutorial/images/TimeWaveToDFT2.jpg"/>

A fast Fourier transform (FFT) is an algorithm that computes the discrete Fourier transform (DFT) of a sequence, or its inverse (IDFT). Fourier analysis converts a signal from its original domain (often time or space) to a representation in the frequency domain and vice versa. 

## Language Used
Python 3.6

## Steps to run
cooley.py file gives the implememntation of the Cooley Tuckey FFT algorithm.

## Psuedo Code
<pre>
X0,...,N−1 ← ditfft2(x, N, s):             DFT of (x0, xs, x2s, ..., x(N-1)s):
    if N = 1 then
        X0 ← x0                                      trivial size-1 DFT base case
    else
        X0,...,N/2−1 ← ditfft2(x, N/2, 2s)             DFT of (x0, x2s, x4s, ...)
        XN/2,...,N−1 ← ditfft2(x+s, N/2, 2s)           DFT of (xs, xs+2s, xs+4s, ...)
        for k = 0 to N/2−1                           combine DFTs of two halves into full DFT:
            t ← Xk
            Xk ← t + exp(−2πi k/N) Xk+N/2
            Xk+N/2 ← t − exp(−2πi k/N) Xk+N/2
        endfor
    endif
    </pre>

## References
<pre>
[1] Gauss, Carl Friedrich (1876) [n.d.]. Theoria Interpolationis Methodo Nova Tractata. Carl Friedrich Gauss Werke. Band 3. Göttingen: Königliche Gesellschaft der Wissenschaften. pp. 265–327.
[2] Heideman, M. T., D. H. Johnson, and C. S. Burrus, "Gauss and the history of the fast Fourier transform," IEEE ASSP Magazine, 1, (4), 14–21 (1984)
[3] Cooley, James W.; Tukey, John W. (1965). "An algorithm for the machine calculation of complex Fourier series". Math. Comput. 19 (90): 297–301. doi:10.2307/2003354. JSTOR 2003354.
</pre>

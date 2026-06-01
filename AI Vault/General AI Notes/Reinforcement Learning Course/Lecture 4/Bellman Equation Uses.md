
To find $V_\pi$ you can use $\pi \times Q_\pi$ for each next state. $\pi$ usually takes the form of $P(a|s)$.
$$ V_\pi(s) = \sum \pi Q_\pi $$
![[Qpi->V.png|500]]


To find $Q_\pi$ you can use $V_\pi \times P(s|a)$.
$$ Q = r_s^a + \gamma (P_{s_1'}^a V_\pi(s_1)+P_{s_2'}^a V_\pi(s_2)+...)$$
![[Pasted image 20260217123703.png|500]]


$$ V_\pi(s_1, a_1) = \text{argmax}(r)+\gamma(\sum_x P(s|a) V^*_x(s_x))$$
![[Pasted image 20260217123734.png|500]]


$$ Q^*(s,a) = r + \gamma \sum P \text{argmax}(Q^*(s', a))$$
![[Pasted image 20260217123804.png|500]]
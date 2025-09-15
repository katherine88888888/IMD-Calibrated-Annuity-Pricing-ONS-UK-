# IMD-Calibrated-Annuity-Pricing-ONS-UK-
Excel-based actuarial model using ONS life tables to price level annuities; it calibrates a decile-specific mortality multiplier (k) to IMD e65, then quantifies fair-value payout differences and interest/retirement-age sensitivities.

<img width="1772" height="603" alt="image" src="https://github.com/user-attachments/assets/25ad6458-18d3-4656-914e-96719ce66808" />


##Methodlody
•	Used ONS life tables (annual death probs qxq_xqx) and scaled them by IMD decile with a single factor kkk: qxadj=1−(1−qx)kq_x^{adj}=1-(1-q_x)^{k}qxadj=1−(1−qx)k.
•	Built an lxl_xlx life table and computed conditional survival from retirement tpr=lr+t/lr{}_{t}p_{r}=l_{r+t}/l_rtpr=lr+t/lr.
•	Priced a level annuity via the annuity factor AFr=∑t≥0tpr (1+i)−(t+(1−d))AF_r=\sum_{t\ge0} {}_{t}p_r \,(1+i)^{-(t+(1-d))}AFr=∑t≥0tpr(1+i)−(t+(1−d)); payout = Lump Sum / AF_r.
•	Produced a current-age valuation by multiplying AFrAF_rAFr by survival to rrr and discounting back to today.
•	Calibrated kkk per decile so model e65 matched ONS e65 (IMD), then compared payouts across deciles and ran interest/retirement-age sensitivities.

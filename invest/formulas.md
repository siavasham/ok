# Earnings Formulas

## 📈 Raw Daily Earnings

```text
Daily_Earning = Base_Return × (1 + Referral_Bonus + TRDX_Bonus)
```

## ⚖️ Liquidity Scaling (if enabled)

```text
Scaling_Factor = MIN(1, Daily_Pool / Total_User_Earnings)
Adjusted_Earning = Daily_Earning × Scaling_Factor
```

> Daily_Pool is calculated from the monthly liquidity cap (e.g. $50,000 / 30).

## 🛡️ Swap Damage (Behavior-Based)

```text
Swap_Rate = Total_Swapped / Total_Earned
Damage_Rate = MIN(Swap_Rate × Damage_Coefficient, Max_Damage)
Claimed_Reward = Adjusted_Earning × (1 - Damage_Rate)
```

> Example: If a user swapped 40% of their total earned and the coefficient is 0.5, they get a 20% penalty on their current reward.

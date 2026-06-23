---
title: "The SAT as a proxy debate over reparations"
date: 2026-06-21

bibliography: "2026-06-23-sat_fairness.yaml"
---

## A fair SAT is impossible

The SAT is intended to predict college success, where higher scores indicate a student is more likely to complete their degree and graduate. 

Let's rescale the scores, so they're between 0 and 1 inclusive. Let's also simplify by supposing our society is stratified into two groups, A and B. These groups might be races, or they might be socioeconomic (Pell grant eligible or not) or they might be based on first gen status. (Below we'll be talking mostly about races, but that's not necessary for the math.) What's important is that the two groups have different true college success rates $Y = 1$: 

$$ r_g = \Pr(Y = 1 | G = g) $$
$$ r_A \neq r_B $$

To be fair predictors of college success in our unfair society, we'd like SAT scores $s$ to satisfy at least three fairness properties: 

(1) Calibration: $\Pr(Y = 1 | score = s, G) = s$

The SAT measures college success, at least probabilistically, and does so in the same way for both groups. 

(2) Negative balance: $\bar{s}_{Y = 0, A} = \bar{s}_{Y = 0, B} = s_{-}$

Among individuals who won't graduate, the average score $s_{-}$ is the same for both groups. If this didn't hold, then we would have disparities in the false positive rate across the two groups. For instance, more A students who won't graduate would be admitted (false positives) than B students who won't graduate. 

(3) Positive balance: $\bar{s}_{Y = 1, A} = \bar{s}_{Y = 1, B} = s_{+}$

This is the same as negative balance, but for students who will graduate. A failure of positive balance might mean more A students who would graduate will be rejected (false negatives) than B students who would graduate. 

In the context of debates over fairness in machine learning, @KleinbergInherentTradeOffsFair2016 showed that no scoring system can satisfy all three of these conditions at once, unless either (1) the true success rates are equal $r_A = r_B$ or (2) the scores are a "perfect predictor."^[Meaning that every positive case (every student who will graduate) gets a score of 1 and every negative case (every student who won't graduate) gets a score of 0.] 

The basic idea of the proof involves two moves. First, calibration implies that each group's average score is equal to its true chance of success $\bar{s}_{G} = r_G$ (which Kleinberg et al. call the group's "base rate"). Second, using the balance requirements, we can derive a formula for base rate in terms of the group-independent positive and negative average scores $s_{+}$ and $s_{-}$: 

$$ r_A = \frac{s_-}{1 - s_+ + s_-} = r_B $$

So either $r_A = r_B$; or $s_+ = 1$ and $s_- = 0$ ("perfection prediction"); or at least one of the fairness properties fails to hold. 

Since there are clear empirical differences in college success rates, and no one expects the SAT to be a perfect predictor, a fair version of the SAT is impossible. We cannot fairly predict college success in our unfair world. 


## Social construction of recidivism and college success

@KleinbergInherentTradeOffsFair2016 and the fairness literature more generally are often framed in terms of predicting recidivism. But recidivism is not a natural kind. Recidivism is often *defined* as committing a crime again^[Note that "recidivism" predictions are often made when someone has been accused and is being considered for release pending trial. At this point in time, the accused has not yet been convicted. So "again" is a mistake.] in the future. But criminality is not a natural kind, much less *future* criminality. There is no innate or essential probability of committing crime at either the individual or group level. 

In addition, recidivism is typically *operationalized* as being arrested again. Substantial racial differences in "true" recidivism risk are due, in the first instance, to cops being more likely to profile Black people. While policy decisions might not completely eliminate racial differences in "true" recidivism risk, it seems highly plausible that policy changes could significantly reduce these differences. In this very concrete sense, recidivism risk is a social construction. 

College success is socially constructed in a similar way. Students from privileged backgrounds are more likely to graduate college than students from marginalized backgrounds because of social policies that tie school funding to the cost of housing and consign impoverished children to chronic malnutrition. In terms of both K-12 preparation and providing support for struggling students, policy could do a lot to reduce differences in the chance of completing a bachelor's degree. 

The transfer of resources from the privileged to the marginalized, in order to equalize opportunity, is *redistribution*. When the groups are racial, redistribution is *reparations*. 

The SAT can only do what its proponents want it do — provide a racially neutral basis for admissions decisions — against a background of reparations. 


## Proxy politics

And yet we do not see SAT proponents advocating for sweeping reforms of our entire educational system. In the UC, the [call to resume the use of the SAT in admissions](https://ucstudentsuccess.org/) is coming from people who seem to be vehemently opposed to offering remedial math and writing courses, which help ensure that all admitted students are up to speed. In their eyes, the UC should not redistribute resources towards underprepared students. That is — since the students who need remedial courses are overwhelmingly from low income communities of color — the UC should not engage in reparations.^[I can imagine some of them might be fine with directing those students towards UC Merced and UC Riverside. At Merced we have lots of seats in the remedial writing and math courses, and the instructors work extremely hard trying to get their students caught up. Of course, this would just intensify the de facto segregation of the UC system: Merced and Riverside are already the two majority-Hispanic, majority-Pell eligible campuses.]  

For proponents of the SAT, its appeal is that it offers the appearance of a racially-neutral and objective measure of college preparedness. We do not need reparations, they think, because we have the SAT. My application of Kleinberg et al.'s result indicates this is mistaken: without reparations, the SAT cannot be racially neutral. 

But for some SAT proponents, the appearance of neutrality may be more important than actual equality of opportunity. The appearance of neutrality allows them to present themselves as color-blind and post-racial. For many centrists, reparations and racial injustice are too controversial, too provocative, best avoided whenever possible. They're talking about the efficient allocation of scarce educational resources, not some wild-eyed proposal for the radical redistribution of wealth. And for the ethnonationalist right, the disparate impact of SAT-based admissions gives them a way to maintain racial segregation without being too blatant even for Samuel Alito. Here, the necessary unfairness of the SAT is a feature, not a bug. 

In other words, the SAT gives some of its advocates a way to oppose the pursuit of racial equality without talking about the reality of racial inequality. The SAT is a proxy for reparations. 


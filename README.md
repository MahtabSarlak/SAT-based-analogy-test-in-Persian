# SAT Based Analogy Evaluation Using ParsBert

We use ParsBert and GPT-2 for answering the analogy test in Persian. An SAT-based analogy test in Persian is gathered by [Mahmoudi et al.](https://arxiv.org/abs/2106.15674) To the best of our knowledge, this is the first study in Persian that attempts to solve an SAT-based analogy test using ParsBert and GPT-2. We examined patterns such as "A to B is like B to MASK". However, the best result was acquired using two-step MASK prediction using ParsBert. During the first step, the relationship between a tuple is extracted. For example, for a sample test like "Tehran to IRAN is like Paris to France", we first predict the relationship between Tehran and IRAN by finding the MASK relation in the pattern "Tehran is MASK of IRAN". We expected that the predicted mask would be "capital". The second step solves the test by considering this pattern: "Capital of France is MASK." Our experiment demonstrated that the proposed method works well on semantic-based tests, whereas it showed poor results on syntactic-based tests.

## Analogy tests

- Analogy Farsi [link](https://github.com/sehsanm/persianslang/blob/master/data/analogy/analogy_farsi.csv)
- Slang analogy test [link](https://github.com/sehsanm/persianslang/blob/master/data/analogy/analogy_slang.csv)
- SAT analogy test [link](https://github.com/sehsanm/persianslang/blob/master/data/analogy/SAT_ANALOGY.csv)
- Bokai analogy test
- Analogy test gathered by Mahmoudi et al. [link](https://github.com/sehsanm/embedding-benchmark/blob/master/data/analogy/analogy.csv)

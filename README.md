[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/SPs4PNWX)
# Lab 1 : CEG 3400 Intro to Cyber Security

## Name: Coleman Fox

### Task 1: Hashing

**Reminder Deliverable:** Is your `salted-data.csv` in this repository?

Answer the following in this file:

* How many unique users are in the data?
	* 42
* How many salts did you create?
	* 42
* How many possible combinations will I need to try to figure out the secret ID
  of all students (assume I know all potential secret IDs and have your 
  `salted-data.csv`)
	* 42^2, or 1764
* Instead of salts, if you were to use a nonce (unique number for each hashed
  field) how many possible combinations would I need to try?
	* 42 times 1303 (the number of entries), which is 54726
* Given the above, if this quiz data were *actual* class data, say for example
  your final exam, how would you store this dataset?  Why?
	* I would store it in a more secure file, one with which only I had access to or one with a password protection. I would do this because this is important data.

```bash
please put any cool bash one-liners or other piped commands you
learned/struggled with for task 1 here
```

---

### Task 2: Crypto Mining

**Reminder Deliverable:** Is your "mining" code in this repository (`mining/`)?
**Reminder Deliverable:** Is your nonce + word combos in `coins.txt`?

Answer the following:

* Paste your ***nonce+word(s) and hash(s)*** below ( either 3x `000` hashes or 1x `0000`
hash)

```

```

* How many words were in your dictionary?
* How many nonces did your code iterate over?
* What was the maximum number of hashes your code *could* compute given the above?
* What did you think about Task 2?
* Is there a better way than brute force to attempt to get higher valued coins?
* Why or why not?


```bash
please put any cool bash one-liners or other piped commands you
learned/struggled with for task 2 here
```


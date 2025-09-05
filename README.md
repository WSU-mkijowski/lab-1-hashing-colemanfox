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
cat salted_data.csv | awk -F ',' '{ print $1}'
```

---

### Task 2: Crypto Mining

**Reminder Deliverable:** Is your "mining" code in this repository (`mining/`)?
**Reminder Deliverable:** Is your nonce + word combos in `coins.txt`?

Answer the following:

* Paste your ***nonce+word(s) and hash(s)*** below ( either 3x `000` hashes or 1x `0000`
hash)

```
00018c2e23b216fccf037ff20a24964c16d684b1ce2a406dc20b360fedcc332e  -, 888orange
000f66376a62aa9435f3249e9d65754d58233f7741983856230732f3d4529b19  -, 3655orange
00049cf9f19572a0d18779189448f7316b977d48edfb4af3d86ca2c64693d852  -, 17960orange

```

* How many words were in your dictionary?
	* I left the dictionary how it came from the initial commit, so 14.
* How many nonces did your code iterate over?
	* My code iterated over 20,000 nonces
* What was the maximum number of hashes your code *could* compute given the above?
	* It could have computed 20,000 hashes
* What did you think about Task 2?
	* I enjoyed Task 2, it helped me understand hashing and datamining further than a surface level understanding.
* Is there a better way than brute force to attempt to get higher valued coins?
	* No
* Why or why not?
	* While you can use additional tools such as scripting, brute force is the best way to get higher value coins because there is no apparent secret to what makes a good nonce/ salt and what doesn't.

```bash
for i in $(seq 20000); do saltedword="$i"orange; hashval=$( echo -n $saltedword | sha256sum); echo "$hashval, $saltedword"; done | grep ^000
```


# ReallyReallyDumbLM
A 15M Dense GQA model trained on UltraFineWeb L3 Multi Style English.
model link : (link)[https://huggingface.co/Leonuraht/ReallyReaallyDumbLM]

Tokenizer : BPE on the same dataset
Vocab : 8192
11 Desnse GQA Blocks wth hdim of 256
Each GQA is 1.2M paras
lr = 8e-4
AdamW optimizer with cosine decay.

## Dataset:
d1 = (0000 + 0001) of UltraFine L3
d2 = (0002 + 0003) of UltraFine L3

Total chars in d1 : 400M approx
Total tokens in d1 : 97 M approx
same goes for d2

each d1 , d2 is trained for 3 epochs.
So total tokens seen : (97 + 97) * 3 = 582M tokens
Which is double its  Chinchilla limit (15 * 20 = 300M tokens) 
the valid loss decreased like:
 4.59 4.08 3.95     3.78 3.58 3.40

**Final Validation : 3.4 -- 3.5**

### After this the model was trained on another 300M dataset and the model valid loss stagnated no the training was stopped.

## Sample Prompt

--- PROMPT: "The history of science shows that" ---
The history of science shows that the term "law" remains evident across its medical societies. The text further includes key concepts and findings, including the concept of the BBC, which aims to illustrate how the term is used in medical settings, the term "law rhym", and the idea of a "laws" meaning "law." The text also references the concept of "law rhym" and "law tatto" in a study used to describe the idea of


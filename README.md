# -Synthesizing-DNA-sequences-with-LLM-


This project is not focused on genome data alone. The purpose is to design a generic solution that may also work
in other contexts, such as synthesizing molecules. The problem involves dealing with a large amount of “text”.
Indeed, the sequences discussed here consist of letter arrangements, from an alphabet that has 5 symbols: A,
C, G, T and N. The first four symbols stand for the types of bases found in a DNA molecule: adenine (A),
cytosine (C), guanine (G), and thymine (T). The last one (N) represents missing data. No prior knowledge of
genome sequencing is required.
The data consists of DNA sub-sequences from a number of individuals, and categorized according to the
type of genetic patterns found in each sequence. Here I combined the sequences together. The goal is to
synthesize realistic DNA sequences, evaluate the quality of the synthetizations, and compare the results with
random sequences. The idea is to look at a DNA string S1 consisting of n1 consecutive symbols, to identify
potential candidates for the next string S2 consisting of n2 symbols. Then, assign a probability to each string
S2 conditionally on S1, use these transition probabilities to sample S2 given S1, then move to the right by n2
symbols, do it again, and so on. Eventually you build a synthetic sequence of arbitrary length. There is some
analogy to Markov chains. Here, n1 and n2 are fixed, but arbitrary.

# Drawing:


# my understanding of the problem
sections of DNA are shared between a ton of individuals. 
I want to create a function that will bin all the data based on where it is on the chromosme and which chromosome it is on. 
Then I want to filter out areas that are shared by a freshold greater than a certain amount.

## questions I have about my understanding
<img width="576" height="324" alt="ibd_pileup_clarification_drawing" src="https://github.com/user-attachments/assets/2b22e7c0-0247-4dfa-aaec-33ef6d2efc48" />
- I coded up a really really quick mock one and it seems like it just ended up filtering out all the segments. 
-  are we supposed to cut out areas that are above the threshold from each of the segments
- OR are we supposed to filter out segments that include the areas that are above the thresholds
- OR a mix of both
- will this cause breakpoints are places that we deem as a cut off

# prewritten options:
1. PLINK (The "Gold Standard")
PLINK is the most widely used tool in genetics. It handles IBD segments (usually in .genome or .segments formats) and can perform "segment pruning."
How it handles your problem: It uses a sliding window to scan the genome. If too many pairs share a segment in a specific window, it can flag or remove them.
Key Command: --homog or --segment-cluster.
Pros: Extremely fast; handles millions of rows in seconds.
Cons: Command-line only; requires converting your data to PLINK format (PED/MAP or BED/BIM/FAM).

2. ERSA (Estimation of Recent Shared Ancestry)
ERSA is specifically designed to solve the "pile-up" problem. It calculates the "background" IBD sharing of a population and filters it out so you only see "true" recent ancestry.
How it handles your problem: It uses a precise statistical model to determine if a shared segment is a "pile-up" (old DNA) or a "match" (recent relative).
Pros: The most scientifically accurate for genealogy.
Cons: It is a research tool (often requiring Linux/Unix) and can be pickier about input formats.

3. IBD-Tracts (The Browning Lab Tools)
Created by the same team that made BEAGLE, these utilities are built specifically for analyzing shared segments.
How it handles your problem: It includes a utility called ibd-frequency which generates a map of how often every single position on a chromosome appears in your IBD file. You can then use this map to "mask" or delete high-frequency areas.

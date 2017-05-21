To learn weights for the entity resolution model, the following command line is used:

learnwts -i er-bnct.mln -t coraSepFixedhwng.1.db,coraSepFixedhwng.2.db,coraSepFixedhwng.3.db,coraSepFixedhwng.4.db -multipleDatabases -o coraSepFixedhwng-learned-can.5.mln -queryEvidence -ne SameBib,SameAuthor,SameTitle,SameVenue -noAddUnitClauses

The flag -queryEvidence tells Alchemy to consider any query predicates not present in .db files as false evidence. This
builds canopies of pairs of citations likely to be the same. The queries not in the .db files can be assumed false with a very high confidence.

Inference can be run using the learned model on the remaining 5th dataset.


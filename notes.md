## 2023-04-04 Pair programming with Aaron: Explicit-key map parsing

- [Un-directed Programming](https://www.sacrideo.us/un-structured-programming/)
- Write what you say: I.e. do-y programming of Scholes' "How to Write Computer Programs"
- Want to be clear about semantic boundaries in data type design
  - APL doesn't contain explicit affordances to signal said boundaries
- Discovered fuzzy semantics around c, s, and e fields
  - c field contains normalized node content
  - s and e fields point to defining input section, to be used in error messages
- Each line of code should have a crisply semantic meaning
  - What am functional sub-pass does the line serve as part of the paragraph?
- Fine-tuning inter-line dependencies in a paragraph
  - Lets us reify semantically-relevant dependencies
  - Breaking dependency might incur re-calculation/verbosity trade-off
- Aaron noticed I moved from thinking about APL mechanics into domain-specific goals
  - E.g. Instead of seeing `2</0,m` as a 2-reduction, it's a head-node selector.
- Next goal: think in terms of operations of whole data, not individual fields
  - Current thought process: Need to update d, k, t, *etc.* of child nodes
  - Target: Need to update child nodes

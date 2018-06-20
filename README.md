# Persistent data structures

## Outline

- Terminology
- Versioning
- Comparison of different approaches
- Fat node method, node-copying method
- Clojure vectors and maps (bit-partitioned array tries & HAMTs),
  path copying
- Recent improvements

## Bibliography

```
@thesis{okasaki1996purely,
  langid = {english},
  title = {Purely Functional Data Structures},
  url = {http://www.cs.cmu.edu/~rwh/theses/okasaki.pdf},
  institution = {{Carnegie Mellon}},
  urldate = {2014-06-01},
  date = {1996},
  author = {Okasaki, Chris}
}

@article{blelloch2001persistent,
  title = {Persistent Triangulations},
  volume = {11},
  url = {https://www.cambridge.org/core/journals/journal-of-functional-programming/article/persistent-triangulations/C7F680713ADE671FB51850F1850B9B2D},
  number = {5},
  journaltitle = {Journal of Functional Programming},
  urldate = {2017-09-29},
  date = {2001},
  pages = {441--466},
  author = {Blelloch, Guy and Burch, Hal and Crary, Karl and Harper, Robert and Miller, Gary and Walkington, Noel}
}

@thesis{dinkla1998geometrische,
  title = {Geometrische {{Algorithmen}} in {{Haskell}}},
  date = {1998},
  author = {Dinkla, Jörn}
}

@article{sarnak1986planar,
  title = {Planar Point Location Using Persistent Search Trees},
  volume = {29},
  url = {http://dl.acm.org/citation.cfm?id=6151},
  number = {7},
  journaltitle = {Communications of the ACM},
  urldate = {2017-09-29},
  date = {1986},
  pages = {669--679},
  author = {Sarnak, Neil and Tarjan, Robert E.}
}

@inproceedings{chuang1993realtime,
  title = {Real-Time Deques, Multihead {{Turing}} Machines, and Purely Functional Programming},
  booktitle = {Proceedings of the Conference on {{Functional}} Programming Languages and Computer Architecture},
  publisher = {{ACM}},
  date = {1993},
  pages = {289--298},
  author = {Chuang, Tyng-Ruey and Goldberg, Benjamin}
}

@online{referencea,
  title = {Reference Request - {{What}}'s New in Purely Functional Data Structures since {{Okasaki}}? - {{Theoretical Computer Science Stack Exchange}}},
  url = {https://cstheory.stackexchange.com/questions/1539/whats-new-in-purely-functional-data-structures-since-okasaki},
  shorttitle = {Reference Request - {{What}}'s New in Purely Functional Data Structures since {{Okasaki}}?},
  urldate = {2017-10-24}
}

@report{bagwell2001ideal,
  title = {Ideal Hash Trees},
  date = {2001},
  author = {Bagwell, Phil}
}

@incollection{kaplan1995persistent,
  title = {Persistent Data Structures},
  booktitle = {Handbook on Data Structures and Applications},
  date = {1995},
  pages = {241--246},
  author = {Kaplan, Haim},
  editorb = {Mehta, Dinesh and Sartaj Sahni},
  editorbtype = {redactor}
}

@misc{sommer2005persistent,
  title = {Persistent {{Data Structures}}},
  url = {https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-854j-advanced-algorithms-fall-2005/lecture-notes/persistent.pdf},
  urldate = {2017-10-24},
  date = {2005},
  author = {Sommer, Gentry and Kohler, Eddie}
}

@report{bagwell2000fast,
  title = {Fast and Space Efficient Trie Searches},
  date = {2000},
  author = {Bagwell, Phil}
}

@inproceedings{steindorfer2015optimizing,
  langid = {english},
  title = {Optimizing Hash-Array Mapped Tries for Fast and Lean Immutable {{JVM}} Collections},
  isbn = {978-1-4503-3689-5},
  url = {http://dl.acm.org/citation.cfm?doid=2814270.2814312},
  doi = {10.1145/2814270.2814312},
  publisher = {{ACM Press}},
  urldate = {2017-12-05},
  date = {2015},
  pages = {783-800},
  author = {Steindorfer, Michael J. and Vinju, Jurgen J.}
}

@unpublished{hickey2008clojure,
  title = {Clojure: {{A Dynamic Programming Language}} for the {{JVM}}},
  date = {2008},
  author = {Hickey, Rich},
  note = {https://www.infoq.com/presentations/hickey-clojure?utm\_source=presentations\_about\_JVMLanguageSummit\&utm\_medium=link\&utm\_campaign=JVMLanguageSummit}
}

@article{prokopec2017cacheaware,
  title = {Cache-Aware Lock-Free Concurrent Hash Tries},
  journaltitle = {arXiv preprint arXiv:1709.06056},
  date = {2017},
  author = {Prokopec, Aleksandar and Bagwell, Phil and Odersky, Martin}
}

@inproceedings{prokopec2012concurrent,
  title = {Concurrent Tries with Efficient Non-Blocking Snapshots},
  volume = {47},
  booktitle = {Acm {{Sigplan Notices}}},
  publisher = {{ACM}},
  date = {2012},
  pages = {151--160},
  author = {Prokopec, Aleksandar and Bronson, Nathan Grasso and Bagwell, Phil and Odersky, Martin}
}

@report{bagwell2011rrbtrees,
  title = {{{RRB}}-{{Trees}}: {{Efficient Immutable Vectors}}},
  shorttitle = {{{RRB}}-{{Trees}}},
  date = {2011},
  author = {Bagwell, Philip and Rompf, Tiark}
}

@inproceedings{prokopec2018cachetries,
  langid = {english},
  title = {Cache-Tries: Concurrent Lock-Free Hash Tries with Constant-Time Operations},
  isbn = {978-1-4503-4982-6},
  url = {http://dl.acm.org/citation.cfm?doid=3178487.3178498},
  doi = {10.1145/3178487.3178498},
  shorttitle = {Cache-Tries},
  publisher = {{ACM Press}},
  urldate = {2018-03-02},
  date = {2018},
  pages = {137-151},
  author = {Prokopec, Aleksandar}
}

@article{driscollmaking,
  langid = {english},
  title = {Making {{Data Structures Persistent}}},
  pages = {39},
  author = {Driscoll, James R. and Sarnak, Neil and Sleator, Daniel D.}
}

@online{expert2013,
  title = {Expert to {{Expert}}: {{Rich Hickey}} and {{Brian Beckman}} - {{Inside Clojure}}},
  url = {https://www.youtube.com/watch?v=wASCH_gPnDw},
  urldate = {2018-06-11},
  date = {2013}
}

@online{lorange2015understanding,
  title = {Understanding {{Clojure}}'s {{Persistent Vectors}}, Pt. 1},
  url = {https://hypirion.com/musings/understanding-persistent-vector-pt-1},
  urldate = {2018-06-12},
  date = {2015-09-25},
  author = {L’orange, Jean Niklas}
}

@online{krukow2009understanding,
  title = {Understanding {{Clojure}}'s {{PersistentHashMap}} (Deftwice...)},
  url = {http://blog.higher-order.net/2009/09/08/understanding-clojures-persistenthashmap-deftwice.html},
  urldate = {2018-06-12},
  date = {2009-09-08},
  author = {Krukow, Karl}
}

@book{emerick2012clojure,
  langid = {english},
  location = {{Sebastopol, Calif}},
  title = {Clojure Programming},
  edition = {1st ed},
  isbn = {978-1-4493-9470-7},
  pagetotal = {607},
  publisher = {{O'Reilly}},
  date = {2012},
  author = {Emerick, Chas and Carper, Brian and Grand, Christophe},
  note = {OCLC: ocn711045678}
}

@article{lorangeimproving,
  langid = {english},
  title = {Improving {{RRB}}-{{Tree Performance}} through {{Transience}}},
  pages = {130},
  author = {L'orange, Jean Niklas}
}

@video{spiewak2011extreme,
  title = {Extreme {{Cleverness}}: {{Functional Data Structures}} in {{Scala}}},
  url = {https://www.infoq.com/presentations/Functional-Data-Structures-in-Scala},
  shorttitle = {Extreme {{Cleverness}}},
  series = {Strange Loop 2011},
  urldate = {2018-06-14},
  date = {2011-12-14},
  director = {Spiewak, Daniel}
}

@inproceedings{conchon2007persistent,
  langid = {english},
  title = {A Persistent Union-Find Data Structure},
  isbn = {978-1-59593-676-9},
  url = {http://portal.acm.org/citation.cfm?doid=1292535.1292541},
  doi = {10.1145/1292535.1292541},
  publisher = {{ACM Press}},
  urldate = {2018-06-14},
  date = {2007},
  pages = {37},
  author = {Conchon, Sylvain and Filliâtre, Jean-Christophe}
}

@online{bierner2014hash,
  title = {Hash {{Array Mapped Tries}} in {{Javascript}} – {{UWTB}}},
  url = {https://blog.mattbierner.com/hash-array-mapped-tries-in-javascript/},
  urldate = {2018-06-17},
  date = {2014-03-06},
  author = {Bierner, Matt}
}

@article{blelloch2015cache,
  langid = {english},
  title = {Cache Efficient Functional Algorithms},
  volume = {58},
  issn = {00010782},
  url = {http://dl.acm.org/citation.cfm?doid=2797100.2776825},
  doi = {10/f7hw38},
  number = {7},
  journaltitle = {Communications of the ACM},
  urldate = {2018-06-18},
  date = {2015-06-25},
  pages = {101-108},
  author = {Blelloch, Guy E. and Harper, Robert}
}

@video{clojuretvstriving,
  title = {Striving to {{Make Things Simple}} and {{Fast}} - {{Phil Bagwell}}},
  url = {https://www.youtube.com/watch?v=K2NYwP90bNs},
  urldate = {2018-06-18},
  director = {{ClojureTV}}
}

@online{pangsakulyanont2016immutable,
  title = {Immutable.Js, Persistent Data Structures and Structural Sharing},
  url = {https://medium.com/@dtinth/immutable-js-persistent-data-structures-and-structural-sharing-6d163fbd73d2},
  journaltitle = {Medium},
  urldate = {2018-06-19},
  date = {2016-12-08T15:28:49.026Z},
  author = {Pangsakulyanont, Thai}
}

@online{reference,
  title = {Reference Request - {{What}} Classes of Data Structures Can Be Made Persistent?},
  url = {https://cs.stackexchange.com/questions/18262/what-classes-of-data-structures-can-be-made-persistent},
  journaltitle = {Computer Science Stack Exchange},
  urldate = {2018-06-19}
}
```

## License

This work is licensed under a Creative Commons Attribution 4.0 International License.

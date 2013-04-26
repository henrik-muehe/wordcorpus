wordcorpus
==========

Word lists extracted from various sources

* `yago2_people.txt` People and the number of articles they are referenced in extracted from the YAGO2 data set using the following query:
    <pre>sparql prefix yago:<http://yago-knowledge.org/resource/>
select ?s (count(?art) as ?count)
 from <http://yago2s.org>
where {
        ?s a/<http://www.w3.org/2000/01/rdf-schema#subClassOf>*
            <http://yago-knowledge.org/resource/wordnet_person_100007846>.
        ?s yago:linksTo ?art
 } ;
 </pre>

  * `wikipedia_*.txt`
 Words extracted from wikipedia and cleaned such that all words are lowercase with only the letters a-z

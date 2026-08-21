# SPARQL WikiData


SPARQL queries
```

SELECT ?person ?personLabel ?image ?dob

WHERE {
    
    #wdt specifies property , #wd specifies value
  
    ?person wdt:P106 wd:Q82955.     # a person whose occupation is politician
    ?person wdt:P39 wd:Q11696.      # position us president
    ?person wdt:P18 ?image.         # image --- in this case we are not specifying the value , instead declaring a var
    ?person wdt:P569 ?dob .         # date of birth --- no specific value , so give it var name
    #?person wdt:P1545 ?ord .
    
  
  SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE],en". }

}

ORDER BY ?personLabel
```

<img width="4020" height="2112" alt="image" src="https://github.com/user-attachments/assets/77c68751-543e-4e4b-aad3-d3cb55b9cb1d" />

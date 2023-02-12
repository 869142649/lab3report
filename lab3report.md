#  grep command

##  1.Searching in all files recursively using grep -r
```
    $  $ grep -r "Lucayans" ./skill-demo1-data/written_2/travel_guides/berlitz2/Bahamas-History.txt              
    ./skill-demo1-data/written_2/travel_guides/berlitz2/Bahamas-History.txt:Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
    ./skill-demo1-data/written_2/travel_guides/berlitz2/Bahamas-History.txt:The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.


    $ grep -r "Italy" skill-demo1-data/written_2/travel_guides 
    skill-demo1-data/written_2/travel_guides/berlitz1/HistoryItaly.txt:        Italy has only existed as a nation since 1871. Before then,
    skill-demo1-data/written_2/travel_guides/berlitz1/HistoryItaly.txt:        and Roman communities in Italy, but know very little of the country’s
    skill-demo1-data/written_2/travel_guides/berlitz1/HistoryItaly.txt:        in Macedonia, Asia Minor, Spain, and southern France. The rest of Italy
    
```

The -r option in grep is used to search for the pattern recursively in all the subdirectories of the specified directory. From the output, we could see the -r option will give us the path, the name of the file, and the line that include the String we search in the files or directory we want.The -r option is useful when you want to search for a pattern in a large number of files.

##  2.Counting the number of matches using grep -c
```
    $ grep -c "Lucayans" ./skill-demo1-data/written_2/travel_guides/berlitz2/Bahamas-History.txt
    2

    $ grep -c "Italy" skill-demo1-data/written_2/travel_guides/berlitz1/WhereToItaly.txt 
    78
```

The -c option for the grep command is used to count the number of lines that match a given pattern.
This command will search the file for lines containing the word "Lucayans" and "Italy", and it will return the count of lines that match the pattern. The result will be a single number representing the count of matching lines, rather than the actual matching lines themselves. The -c option is useful when you just want to get the count of the String.


##  3.Display only the file names which matches the given pattern using grep -l
```
    $ grep -l ".java" *
    FileHelpers.class
    FileServer.class
    FileServer.java
    FileServerTests.java
    Handler.class
    Read.java
    Server.class
    Server.java
    ServerHttpHandler.class
    URLHandler.class


    $ grep -l Luck *
    grep: lab3report: Is a directory
    grep: lib: Is a directory
    grep: quiz-layout: Is a directory
    grep: skill-demo1-data: Is a directory
    grep: some-files: Is a directory
    grep: test-data: Is a directory

```
The -l option for the grep command is used to list the names of files that contain lines that match the specified pattern, rather than the actual matching lines themselves. For the first example, this command will search all files in the current directory for lines containing the pattern ".java". The -l option will cause grep to only print the names of files that contain a match, rather than the actual matching lines. It there is no match, it will print all directory. It will be very useful when you try to find some common pattern in your whole directory structure.

##  4.Display the matched lines, but do not display the filenames using grep -h
```
    $  grep -h "Lucayans" ./skill-demo1-data/written_2/travel_guides/berlitz2/Bahamas-History.txt
    Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
    The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.

    grep -h "Italy" skill-demo1-data/written_2/travel_guides/berlitz1/WhereToItaly.txt 
        decisions. “ Doing” Italy is a lifetime job, and many devotees are so
        principal city as a focus or starting point: Rome for central Italy,
        Given the sheer and unrivaled richness of Italy, the
        Italy well will inevitably feel that a few of their favorite spots have
        magical romance of Venice. For many, the key to Italy’s Mediterranean
        different facets of Italy’s daily life. Nowhere is it easier or more
        delightful to overdose on museums and monuments than in Italy. A dear
        old lady returned from her first visit with the observation: “Italy’s
        chronicling the unparalleled glories of Italy’s history, the best way
        Many people cannot manage to go to Italy outside the major
        economy, Italy has an elaborate network of information offices.
        cities as well as regional capitals. When in Italy, look instead for
        through Italy, but here are some general thoughts to help you plan your
        Try to vary the kind of places that you stay in. Italy has
        The center of Italy is the cradle of Latin civilization,
        the new king of Italy after 1870, and since 1947 is the presidential
        first king of unified Italy as well as the Tomb of the Unknown Soldier
        Renaissance masters such as Raphael as well as the first king of Italy
        lira every year and provide a palace in Paris as Italy’s embassy.
        of Italy only since the Lateran Treaty signed by Mussolini in 1929.
        The largest collection of Etruscan art in Italy can be
        park. One of Italy’s loveliest and most important small museums, its
        (rarely first-time visitors to Italy) should consider summertime stays
        island is one of Italy’s smartest resort areas, with beautiful beaches,
        that make up the open-air Mercato San Lorenzo, one of Italy’s largest
        leads to the richest of Italy’s art museums, the Uffizi. At the south
        chamber of Italy’s first national parliament. The décor celebrates
        the third of Italy’s three Renaissance giants, Raphael, brings his own
        The church also boasts one of Italy’s most delightful
        today: This is some of Italy’s finest window shopping. A bronze bust
        (1900) of Italy’s most celebrated goldsmith, Benvenuto Cellini, holds a
        the 14th centuries, is for many the greatest of Italy’s, possibly all
        the 16th century, and held sway until the unification of Italy. Apart
        turned his native pink-hued town into Italy’s major pilgrimage
        universities (its state university, one of Italy’s largest, was founded
        grandest civic edifices in all Italy, and from the piazza and the
        Throughout Italy’s history, its northeast regions have
        Franchetti Museum. Italy’s most impressive post office, Fondaco dei
        residence that is one of Italy’s most romantic (the romantic lobby bar
        the 18th century of its gentle decadence. One of Italy’s most important
        charming back roads; this is one of Italy’s principal wine growing
        the most elaborate Gothic funerary monuments in Italy.
        The landscape of Italy’s eastern Alps is a mixture of rich
        of San Petronio ranks among the most imposing of Italy’s Gothic
        called on the greatest artists both from Italy and beyond, from
        Hugging the slopes of Mont Blanc (Monte Bianco), Courmayeur is Italy’s
        design (1925–1931), the Pirelli skyscraper, opposite, (Italy’s first),
        Italy.
        Italy’s Flamboyant Gothic cathedrals. Teams of Italian, French,
        northern Italy. In its fine arcaded courtyard, notice a bronze statue
        On a more sentimental note, Italy’s Lake District at the
        One of Italy’s finest, the Galleria dell’Accademia Carrara
        that his design was inspired by the contours of the lake. But Italy’s
        Italy’s reigning royal family from 1861 to 1946, with Turin serving
        ever so briefly as the capital of the newly unified Italy in 1861.
        than the rest of Italy. But whatever Gallic ambience this may have
        the 17th and 18th centuries was accompanied by Italy’s first coherent
        times. It is one of the most comprehensive of its kind in Italy. Then
        cherishes one of Italy’s most celebrated (and controversial) relics,
        European paintings, making this collection one of Italy’s richest. It
        skiing in winter. This is Italy’s oldest ski resort and an Alpine
        to turn its back on Italy and seek its fortune on the high seas. This
        With 28 km (17 miles) of docks, Italy’s biggest port
        that provide some of Italy’s loveliest treks.
        marble quarries provided the raw material for Italy’s greatest
        it is still virgin land for the majority of Italy’s visitors. It has
        beautiful Amalfi coast. Otherwise, southern Italy is overlooked by
        life. In the outdoor theater that is Italy, Naples is unabashed
        remotely interested in southern Italy’s Greek, Etruscan, and Roman
        Italy. They include Clients Consulting a Sorceress and Strolling
        oldest surviving in Italy, offering a fine view back over the town from
        Italy has no more magnificent testimony of its Greek
        Italy’s boot, endowed with a wild and unspoiled beauty over the gently
        this end-of-the-world piece of Italy is still part of Europe.
        is generally of the sun-and-sea kind, as it is one of Italy’s most
        ways a country to itself, seemingly not part of Italy or Europe at all,
        achievements in Italy, the 12th-century Palatine Chapel (Cappella
        Ravenna, they are Italy’s finest. The combination of figurative and

The option "-h" is used to suppress the printing of file names in the output. This means that when using "grep -h", the name of the file in which a match was found will not be displayed, only the matching lines will be displayed. It is useful when you are using grep in a script or a pipeline, and you want the output to be in a consistent and easily parsable format. The absence of file names in the output helps in this regard.



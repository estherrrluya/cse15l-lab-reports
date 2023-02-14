# Lab Report 3

In this lab report, I will introduce some command-line options for *grep* with examples.

## Command-line options with *Grep*

The following are the four ways to use *grep*:
1. *-i*
2. *-rl*
3. *-n*
4. *-v*

### Example 1 - *-i*

```
Esthers-MacBook-Air:travel_guides esther$ grep -i "Royale" berlitz2/Nepal-WhatToDo.txt
Kathmandu also has several casinos, including Casino Nepal at the Soaltee Crowne Plaza Kathmandu, Casino Everest at the Everest Hotel, Casino Royale at 
the Hotel Yak & Yeti, and Casino Anna at the Hotel de l’Annapurna. All of these casinos are off limits to Nepalis, who are nonetheless fanatical gamblers
at cards, particularly during the Dasain and Tihar festivals. The casino clientele consists primarily of rich Indian visitors who fill the gaming tables 
and slot-machine jungles. A free taxi ride back to your hotel is provided at night. The Casino Royale is housed in a former palace and is the most 
impressive of the city’s casinos.
```

### Example 2 - *-i*

```
Esthers-MacBook-Air:travel_guides esther$ grep -i "royale" berlitz2/Nepal-WhatToDo.txt
Kathmandu also has several casinos, including Casino Nepal at the Soaltee Crowne Plaza Kathmandu, Casino Everest at the Everest Hotel, Casino Royale at 
the Hotel Yak & Yeti, and Casino Anna at the Hotel de l’Annapurna. All of these casinos are off limits to Nepalis, who are nonetheless fanatical gamblers
at cards, particularly during the Dasain and Tihar festivals. The casino clientele consists primarily of rich Indian visitors who fill the gaming tables
and slot-machine jungles. A free taxi ride back to your hotel is provided at night. The Casino Royale is housed in a former palace and is the most 
impressive of the city’s casinos.
```

So, the *-i* option allows you search something in a case-insensitive manner. Whether I typed "Royale" or "royale", the output is the same. It is useful as it allows you search a specific string in the file that it doesn't matter if it's capitalized or not.

#### Source: 
I asked chatGpt and also searched through this document about grep: 
[GNU Grep 3.8](https://www.gnu.org/software/grep/manual/grep.html)

### Example 3 - *-rl*

```
Esthers-MacBook-Air:CSE-15L-Wk4 esther$ grep -rl "Royale" written_2/
written_2//travel_guides/berlitz1/WhatToFWI.txt
written_2//travel_guides/berlitz1/WhereToFrance.txt
written_2//travel_guides/berlitz2/Canada-WhereToGo.txt
written_2//travel_guides/berlitz2/Paris-WhereToGo.txt
written_2//travel_guides/berlitz2/CanaryIslands-WhatToDo.txt
written_2//travel_guides/berlitz2/Nepal-WhatToDo.txt
```

### Example 4 - *-rl*

```
Esthers-MacBook-Air:CSE-15L-Wk4 esther$ grep -rl "Hamilton" written_2/
written_2//non-fiction/OUP/Abernathy/ch2.txt
written_2//non-fiction/OUP/Kauffman/ch6.txt
written_2//non-fiction/OUP/Kauffman/ch10.txt
written_2//travel_guides/berlitz1/WhereToEdinburgh.txt
written_2//travel_guides/berlitz2/Canada-WhereToGo.txt
written_2//travel_guides/berlitz2/Bermuda-WhatToDo.txt
written_2//travel_guides/berlitz2/Canada-History.txt
written_2//travel_guides/berlitz2/Bermuda-history.txt
written_2//travel_guides/berlitz2/Bermuda-WhereToGo.txt
```

So, the *-r* (or --recursive) is an option that causes grep to search through all files in a directory, including subdirectories, recursively. The *-l* 
option can be combined with the *-r* option to become *-rl* that allows searching through also subdirectories and display the name of the file. It is 
useful when you only want to know which files contain the search string but not the actual content by searching recursively through all the files even
within the subdirectories.

#### Source: 
I asked chatGpt and also searched through this document about grep:
[GNU Grep 3.8](https://www.gnu.org/software/grep/manual/grep.html)

### Example 5 - *-n*

```
Esthers-MacBook-Air:CSE-15L-Wk4 esther$ grep -n  "Hamilton" written_2//travel_guides/berlitz1/WhereToEdinburgh.txt
489:        in by royalty. It belongs to the Hamilton family, who have served as
```

### Example 6 - *-n*

```
Esthers-MacBook-Air:CSE-15L-Wk4 esther$ grep -n  "hurricanes" written_2//travel_guides/berlitz2/Bermuda-WhereToGo.txt
106:At the top of King Street is State House, built in the 1620s to house Bermuda’s Assembly. Today it is the oldest stone building on the island. The 
plain façade and sturdy walls were designed to withstand hurricanes and the worst of the summer humidity. It was used continuously until 1815, when the 
island’s capital was moved from St. George’s to Hamilton. The local Masonic lodge negotiated with the Assembly to use the building, with a rent of one 
peppercorn per year, a price that remains in force to this day. The “peppercorn” rent is handed over to the crown in one of the most ornate ceremonial 
occasions of the year, with the mayor and town officials in full official regalia.
```

So, the option *-n* displys the line number of the matching lines for the string being searched. It is useful when you want to know the line number of the matching lines.

#### Source: 
I asked chatGpt and also searched through this document about grep: 
[GNU Grep 3.8](https://www.gnu.org/software/grep/manual/grep.html)

### Example 7 - *-v*

```
Esthers-MacBook-Air:CSE-15L-Wk4 esther$ grep -v "Hotels" written_2/travel_guides/berlitz1/HandRIbiza.txt   
      
        The establishments listed below offer a cross-section of
        local restaurants, and should convince you that not everything on the
        island comes with chips (french fries).
        The star rating in brackets after each entry refers to the
        offfical government rating system.
        As a basic guide, the symbols we use indicate what you can
        expect to pay for a three-course meal for two, excluding wine, tax and
        tip. Drinks will add considerably to the final bill.
        ✪less than 5,000 ptas.
        ✪✪5,000–8,000 ptas.
        ✪✪✪more than 8,000 ptas.
```

### Example 8 - *-v*

```
Esthers-MacBook-Air:CSE-15L-Wk4 esther$ grep -v "Istanbul" written_2/travel_guides/berlitz1/HandRIstanbul.txt
      
        Recommended Hotels
        the city has recently seen a boom in the hotel business. However, if
        you want a room in a particular hotel, it is best to book, especially
        during July and August. The main hotel areas are Laleli, Aksaray, and
        Sultanahmet in the Old City, and around Taksim Square in Beyo‘lu.
        Intense competition among the middle-range hotels means that you can
        often bargain for a lower rate, especially if you plan to stay for more
        than two nights.
        As a basic guide we have used the symbols below to indicate
        prices for a double room with bath, including breakfast:
        ❁❁❁❁❁over £130 ($200)
        ❁❁❁❁£80–130 ($120-200)
        ❁❁❁£50–80 ($75-120)
        ❁❁£30–50 ($45-75)
        ❁below £30 ($45
```
So, the option -v (invert match) makes grep search for lines that do not match the specified pattern. It is useful when you want to exclude certain lines from the output.

#### Source: 
I asked chatGpt and also searched through this document about grep: 
[GNU Grep 3.8](https://www.gnu.org/software/grep/manual/grep.html)

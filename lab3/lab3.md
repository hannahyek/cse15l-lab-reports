# Lab Report 3 - Researching Commands

For this report, I have chose to look into the `find` command and alternate ways to implement this command. Each of the following interesting command-line options were found at [GeeksforGeeks](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/).

## 1. Search a file with a specific name.
- The `-name` option will search for a file with a specific name in a given directory.
- For example, the following code blocks are searching the `written_2` directory for the specified filename.
```
$ find ./written_2 -name HandRHawaii.txt
./written_2/travel_guides/berlitz1/HandRHawaii.txt
```
> Here, the `find` command is searching the directory `written_2` and the `-name` option poses the condition that the name of the file must be `HandRHawaii.txt`. This is useful as it lets us know the path of specific files.
```
$ find ./written_2 -name ch1.txt
./written_2/non-fiction/OUP/Abernathy/ch1.txt
./written_2/non-fiction/OUP/Berk/ch1.txt
./written_2/non-fiction/OUP/Fletcher/ch1.txt
./written_2/non-fiction/OUP/Kauffman/ch1.txt
./written_2/non-fiction/OUP/Rybczynski/ch1.txt
```
> Similarly, the `-name ch1.txt` command restricts the `find` command to search the directory for files with that specific name. As we can observe, there are multiple files with the same name under different paths and this option informs us of all of them.

## 2. Search a file with a pattern.
- We are able to search for files with a designated pattern using the `-name` option by utilizing the asterisk (*).
```
$ find ./written_2 -name "ch*.txt"
./written_2/non-fiction/OUP/Abernathy/ch1.txt
./written_2/non-fiction/OUP/Abernathy/ch14.txt
./written_2/non-fiction/OUP/Abernathy/ch15.txt
./written_2/non-fiction/OUP/Abernathy/ch2.txt 
./written_2/non-fiction/OUP/Abernathy/ch3.txt 
./written_2/non-fiction/OUP/Abernathy/ch6.txt 
./written_2/non-fiction/OUP/Abernathy/ch7.txt 
./written_2/non-fiction/OUP/Abernathy/ch8.txt 
./written_2/non-fiction/OUP/Abernathy/ch9.txt 
./written_2/non-fiction/OUP/Berk/ch1.txt      
./written_2/non-fiction/OUP/Berk/ch2.txt      
./written_2/non-fiction/OUP/Berk/ch7.txt      
./written_2/non-fiction/OUP/Castro/chA.txt    
./written_2/non-fiction/OUP/Castro/chB.txt    
./written_2/non-fiction/OUP/Castro/chC.txt    
./written_2/non-fiction/OUP/Castro/chL.txt    
./written_2/non-fiction/OUP/Castro/chM.txt    
./written_2/non-fiction/OUP/Castro/chN.txt    
./written_2/non-fiction/OUP/Castro/chO.txt    
./written_2/non-fiction/OUP/Castro/chP.txt    
./written_2/non-fiction/OUP/Castro/chQ.txt    
./written_2/non-fiction/OUP/Castro/chR.txt    
./written_2/non-fiction/OUP/Castro/chV.txt    
./written_2/non-fiction/OUP/Castro/chW.txt    
./written_2/non-fiction/OUP/Castro/chZ.txt
./written_2/non-fiction/OUP/Fletcher/ch1.txt
./written_2/non-fiction/OUP/Fletcher/ch10.txt
./written_2/non-fiction/OUP/Fletcher/ch2.txt
./written_2/non-fiction/OUP/Fletcher/ch5.txt
./written_2/non-fiction/OUP/Fletcher/ch6.txt
./written_2/non-fiction/OUP/Fletcher/ch9.txt
./written_2/non-fiction/OUP/Kauffman/ch1.txt
./written_2/non-fiction/OUP/Kauffman/ch10.txt
./written_2/non-fiction/OUP/Kauffman/ch3.txt
./written_2/non-fiction/OUP/Kauffman/ch4.txt
./written_2/non-fiction/OUP/Kauffman/ch5.txt
./written_2/non-fiction/OUP/Kauffman/ch6.txt
./written_2/non-fiction/OUP/Kauffman/ch7.txt
./written_2/non-fiction/OUP/Kauffman/ch8.txt
./written_2/non-fiction/OUP/Kauffman/ch9.txt
./written_2/non-fiction/OUP/Rybczynski/ch1.txt
./written_2/non-fiction/OUP/Rybczynski/ch2.txt
./written_2/non-fiction/OUP/Rybczynski/ch3.txt
```
> In this case, there is a search for files that are named `ch*.txt` where the `*` can be replaced by any assortment of characters. This is useful for finding files with patterned names.
```
$ find ./written_2 -name "History*.txt"
./written_2/travel_guides/berlitz1/HistoryDublin.txt
./written_2/travel_guides/berlitz1/HistoryEdinburgh.txt
./written_2/travel_guides/berlitz1/HistoryEgypt.txt
./written_2/travel_guides/berlitz1/HistoryFrance.txt
./written_2/travel_guides/berlitz1/HistoryFWI.txt
./written_2/travel_guides/berlitz1/HistoryGreek.txt
./written_2/travel_guides/berlitz1/HistoryHawaii.txt
./written_2/travel_guides/berlitz1/HistoryHongKong.txt
./written_2/travel_guides/berlitz1/HistoryIbiza.txt
./written_2/travel_guides/berlitz1/HistoryIndia.txt
./written_2/travel_guides/berlitz1/HistoryIsrael.txt
./written_2/travel_guides/berlitz1/HistoryIstanbul.txt
./written_2/travel_guides/berlitz1/HistoryItaly.txt
./written_2/travel_guides/berlitz1/HistoryJamaica.txt
./written_2/travel_guides/berlitz1/HistoryJapan.txt
./written_2/travel_guides/berlitz1/HistoryJerusalem.txt
./written_2/travel_guides/berlitz1/HistoryLakeDistrict.txt
./written_2/travel_guides/berlitz1/HistoryLasVegas.txt
./written_2/travel_guides/berlitz1/HistoryMadeira.txt
./written_2/travel_guides/berlitz1/HistoryMadrid.txt
./written_2/travel_guides/berlitz1/HistoryMalaysia.txt
./written_2/travel_guides/berlitz1/HistoryMallorca.txt
```
> We can see another application of the asterisk under the `-name` option when searching for history text files in the `written_2` directory. This produces all the paths for history text files in an orderly manner.

## 3. Search for empty files and directories.
- The `-empty` option allows us to find all empty folder and files in the given directory.
```
$ find ./written_2 -empty
```
> If we wanted to check a directory for empty files for the purpose of removing them, the `-empty` option will grant us a list of file paths to empty files/directories. Here, we can see that `written_2` has 0 empty files/subdirectories.
```
$ find ./written_2/travel_guides -empty
```
> This command further comfirms the fact that `written_2` contains no empty files as it is searching its subdirectory `travel_guides` for empty files. The lack of output is due to there being none.

## 4. Search text within multiple files.
```
$ find ./written_2 -type f -name "*.txt" -exec grep 'Lucayans'  {} \;
Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```
> There are multiple options being used in this command. From left to right,  `-type f` specifies the input type is a file, `-name "*.txt"` searches for files ending in .txt, and `-exec grep 'Lucayans'` is used to execute the grep command to print lines which have the input string in them. This is useful for finding specific information on certain topics.
```
$ find ./written_2 -type f -name "*.txt" -exec grep 'Oahu'  {} \;
        Oahu (Including Honolulu)
        on the west side of Oahu, expertly managed by JW Marriott, Ihilani is
        a cannon and ship. Maui fell first, followed by Oahu, Lanai, and
        sands of Oahu; and jet air service brought in vacationers by the
        islands — Oahu, Maui, Kauai, and the Big Island of Hawaii. Some
        Oahu: Waikiki Beach is the tourist center of the islands,
```
> The same concept is applied with this command but to search on information regarding Oahu. The content inside the curly braces `{}` is responsible for replacing each file name found when the command is executed and the `\;` indicates the end of the executed pattern.



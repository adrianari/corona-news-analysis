# Data collection and cleaning

How I collected the data and how I prepocessed it.

## Folder structure
A comprehensive description on what to find where.

### 1-scrapers
<b> INPUT FILES:</b>  None required <br>
<b> OUTPUT FILES: </b> Python list containing the links to the articles of interest, csv-file(s) containing the full articles and where available the comments

Find all the scrapers to the following Swiss online news media and their handle in the further continuation / code:

<li> blick.ch / blick </li>
<li> luzernerzeitung.ch / nlz</li>
<li> nau.ch / nau </li>
<li> nzz.ch / nzz </li>
<li> tagesanzeiger.ch / tagi </li>
<li> watson.ch  / watson </li>
<li> woz.ch / woz </li>

<br>
Per online news medium, there is a NAME-sitegetter.ipynb script as well as a NAME-contentgetter.ipynb script. Where there was an online comment function, there is also a NAME-commentgetter.ipynb script.

Before running the scripts / scraping, please make sure that you have the read the according terms and condition of the media plattform of interest plus that you have permission to scrape from the according site. Furthermore, where required you will need to create a login or a subscription.

<br>

### 2-department-ressort-creation 
<b> INPUT FILES: </b> None required <br>
<b> OUTPUT FILES: </b>  2 python lists, containing the reclassification list (ressorts_cat.bin) and the list with the categories to delete. 

Reclassifies all the categories in which an article is published to classical news departments / ressorts and classifies such articles that are about videos as data to delete (to_delete.bin). Latter is done as with such articles, we do not expect much text to analyze but only videos) 

<br>

### 3-data-cleaning-articles
<b>INPUT FILES:</b> 
<li> csv-file(s) of the articles </li>
<li> ressorts_cat.bin </li>
<li> to_delete.bin </li
 <p></p>
<b> OUTPUT FILES:</b>  Dataframe with all the articles per news outlet as csv
<p></p>
Standard data cleaning process. Not to be mistaken with text preprocessment in an NLP way of understanding.
<br>
<p></p>
 
### 4-data-cleaning-comments
<b>INPUT FILES:</b> 
<li> csv-file(s) of the comments </li>
<li> ressorts_cat.bin </li>
<li> to_delete.bin </li
<p></p>
<b> OUTPUT FILES:</b>  Dataframe with all the comments per news outlet as csv.
<p></p>
Standard data cleaning process. Not to be mistaken with text preprocessment in an NLP way of understanding.



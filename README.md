# Urban-Sport-Field-Keyword-Analysis

#### 1. Web Scraping with Selenium & REST API(Naver API)
#### 2. Text Classification with Bi-directional LSTM
#### 3. LDA Topic Modeling

## Goal of the project
1. Figure out keywords or topic from review of urban sport field in major cities in Korea.
2. Scrap more than 10k data with REST API, and make the automated scrapping process.
3. Use various text analysis modeling method.

## Packages/Library used
<table>
<tbody>
    <tr>
        <td width="60">
            <div align="center"><a href="https://www.python.org/" target="_blank"> <img src="https://github.com/miniwa00/Urban-Sport-Field-Keyword-Analysis/assets/47784464/1a026bce-a19e-40cd-b2c9-a72f0e8050bf" alt="python" width="40" height="40"/> </a><br>Python3</br></div>
        </td>
        <td>
            <div align="center"><a href="https://babeljs.io/" target="_blank"> <img src="https://studygyaan.com/wp-content/uploads/2021/12/Python-Socket-IO.jpg?ezimgfmt=rs:300x150/rscb1/ng:webp/ngcb1" alt="babel" width="40" height="40"/> 
            </a><br>Python Socket</br></div>
        </td>
        <td>
            <div align="center"><a href="https://docs.python.org/ko/3/library/json.html" target="_blank"> <img src="https://velog.velcdn.com/images/swhan9404/post/c43940fd-06ab-4fe6-b905-df695506ce8c/d2f1b26783.png" alt="babel" width="40" height="40"/> 
            </a><br>Python Json</br></div>
        </td>
</tbody>
</table>

## 1. Web Scraping with Selenium & REST API(Naver API)
- I Scraped 10k data from Naver Blog when searched for 'Sport field'
- You can manually input any query. Than you can get 1100 data at once. But it takes some time (about 10+ min)
- It is impossible to get More than 1100 data due to the Naver API policy. If you want so, you can use Beatiful Soup or else.
- Now is cleansing time. There are so many HTML/CSS tags and special chars. I made four function, so you can easily do cleansing.

## 2. Text Classification with Bi-directional LSTM
- When you check the df that you've just got at the last step, you can find that many irrelevant data to reviews. So we have to classify it.
- It's a similar to spam mail classification. **So I used RNN**.
- But It showed 

## 3. LDA Topic Modeling
- I did LDA topic modeling to figure out topics and keywords from corpus of reviews.
- First, I tokenized and lemmatized contents of all reviews. And vertorized them.
- Second, I made a function that shows confusion by number of topics just like the png below.
<img src="https://github.com/miniwa00/Urban-Sport-Field-Keyword-Analysis/assets/47784464/1a026bce-a19e-40cd-b2c9-a72f0e8050bf" width="500" height="350"/>
- So we can see that **18 topics** are the best.

## Result


# Urban-Sport-Field-Keyword-Analysis

#### 1. Web Scraping with Selenium & REST API(Naver API)
#### 2. Text Classification with Bi-directional LSTM
#### 3. LDA Topic Modeling

## Goal of the project
1. Figure out keywords or topic from review of urban sport field in major cities in Korea.
2. Scrap more than 10k data with REST API, and make the automated scrapping process.
3. Use various text analysis modeling method.

## Packages/Library used

**Mainly**
<table>
<tbody>
    <tr>
        <td width="60">
            <div align="center"><a href="https://www.python.org/" target="_blank"> <img src="https://github.com/miniwa00/Urban-Sport-Field-Keyword-Analysis/assets/47784464/f8ac5984-af72-4233-9045-08df71a7cbf4" alt="python" width="100" height="45"/> 
            </a><br>Python3</br></div>
        </td>
        <td>
            <div align="center"><a href="https://babeljs.io/" target="_blank"> <img src="https://github.com/miniwa00/Urban-Sport-Field-Keyword-Analysis/assets/47784464/0b29652b-0c8a-4d9a-8e0d-a639ef814cfd" alt="babel" width="70" height="40"/> 
        </a><br>Jupyter Notebook</br></div>
        </td>
        <td>
            <div align="center"><a href="https://babeljs.io/" target="_blank"> <img src="https://github.com/miniwa00/Urban-Sport-Field-Keyword-Analysis/assets/47784464/39bdc13a-d6e6-41a3-b3a4-fb34eb6bc70b" alt="babel" width="80" height="40"/> 
            </a><br>Scikit-Learn(LDA)</br></div>
        </td>
</tbody>
</table>

**Web Scraping**
<table>
<tbody>
    <tr>
        <td width="60">
            <div align="center"><a href="https://www.python.org/" target="_blank"> <img src="https://github.com/miniwa00/Urban-Sport-Field-Keyword-Analysis/assets/47784464/54a2d184-3716-4c4d-b4a5-715e649b02a0" alt="python" width="40" height="40"/> 
            </a><br>Selenium</br></div>
        </td>
        <td>
            <div align="center"><a href="https://babeljs.io/" target="_blank"> <img src="https://github.com/miniwa00/Urban-Sport-Field-Keyword-Analysis/assets/47784464/098283aa-084a-4082-8d06-fff8eb429782" alt="babel" width="70" height="40"/> 
            </a><br>Beatiful Soup</br></div>
        </td>
        <td>
            <div align="center"><a href="https://babeljs.io/" target="_blank"> <img src="https://github.com/miniwa00/Urban-Sport-Field-Keyword-Analysis/assets/47784464/6c8fb542-4dde-4b60-8fee-ca87620e1088" alt="babel" width="140" height="70"/> 
            </a><br>Naver API</br></div>
        </td>
</tbody>
</table>

**Text Classification - Bidirectioanl LSTM, Vanilla LSTM**
<table>
<tbody>
    <tr>
        <td width="60">
            <div align="center"><a href="https://www.python.org/" target="_blank"> <img src="https://github.com/miniwa00/Urban-Sport-Field-Keyword-Analysis/assets/47784464/771a8263-432d-4d2b-a9bf-2768bf847ceb" alt="python" width="100" height="50"/> 
            </a><br>TensorFlow</br></div>
        </td>
        <td>
            <div align="center"><a href="https://babeljs.io/" target="_blank"> <img src="https://github.com/miniwa00/Urban-Sport-Field-Keyword-Analysis/assets/47784464/8af421b6-f924-41a6-8867-77e3097d011f" alt="babel" width="70" height="40"/> 
            </a><br>Keras</br></div>
        </td>
        <td>
            <div align="center"><a href="https://babeljs.io/" target="_blank"> <img src="https://github.com/miniwa00/Urban-Sport-Field-Keyword-Analysis/assets/47784464/39bdc13a-d6e6-41a3-b3a4-fb34eb6bc70b" alt="babel" width="80" height="40"/> 
            </a><br>Scikit-Learn(CountVectorizer)</br></div>
        </td>
</tbody>
</table>

**Text Preprocessing**

<table>
<tbody>
    <tr>
        <td width="60">
            <div align="center"><a href="https://www.python.org/" target="_blank"> <img src="https://github.com/miniwa00/Urban-Sport-Field-Keyword-Analysis/assets/47784464/ac0d12f0-9db6-4fe7-be05-214cd7db500d" alt="python" width="100" height="50"/> 
            </a><br>Konlpy</br></div>
        </td>
        <td>
            <div align="center"><a href="https://babeljs.io/" target="_blank"> <img src="https://github.com/miniwa00/Urban-Sport-Field-Keyword-Analysis/assets/47784464/83434a59-3d87-4a87-b3e2-bdbc4823c12c" alt="babel" width="50" height="50"/> 
            </a><br>Pykospacing</br></div>
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
<img src="assets/topic_result.png" width=550 height=300/>

- Interpretation of topics may vary depending on what meaning the user is looking for.


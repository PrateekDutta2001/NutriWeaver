# NutriWeaver

Find the full repo access at [Click here](https://drive.google.com/drive/folders/1gBTeLLuSCv9IAk8UQorsGG1i9hQNKUk_?usp=sharing)

**Motivation**

People from all around the world are getting more concerned in their health and way of life in today's modern environment. However, avoiding junk food and exercising alone are insufficient; we also need to eat a balanced diet. We can live a healthy life with a balanced diet based on our height, weight, and age. Your diet can help you achieve and maintain a healthy weight, lower your chance of developing chronic diseases (including cancer and heart disease), and improve your general health when combined with physical activity. Nevertheless, there is a little SOTA project on food/diet recommendation system. Therefore I got the idea to build a content-based recommendation system for this purpose using machine learning.

**What is NutriWeaver?**

NutriWeaver is a content-based approach which is an important tool for promoting healthy eating habits. This type of engine uses information about the nutritional content and ingredients of foods to make personalized recommendations to users. One of the key advantages of a content-based approach is that it takes into account an individual's dietary restrictions and preferences, such as allergies or food preferences. By providing users with tailored recommendations, a content-based food recommendation engine can help them make better choices about what to eat and improve their overall health. Additionally, by recommending a variety of healthy foods, it can also help users to discover new and nutritious options, expand their dietary horizons and overcome food boredom. All these can lead to a better and well-rounded diet, which can have a positive impact on long-term health outcomes.

**What is content based recommendation engine?**

A content-based recommendation engine is a type of recommendation system that uses the characteristics or content of an item to recommend similar items to users. It works by analyzing the content of items, such as text, images, or audio, and identifying patterns or features that are associated with certain items. These patterns or features are then used to compare items and recommend similar ones to users.

**Why content-based approach?**

- No data from other users is required to start making recommendations.
- Recommendations are highly relevant to the user.
- Recommendations are transparent to the user.
- You avoid the “cold start” problem.
- Content-based filtering systems are generally easier to create.

**Challenges of content-based approach**

- There’s a lack of novelty and diversity.
- Scalability is a challenge.
- Attributes may be incorrect or inconsistent.

# Developement

The recommendation engine is built using Nearest Neighbors alogrithm which is an unsupervised learner for implementing neighbor searches. It acts as a uniform interface to three different nearest neighbors algorithms: BallTree, KDTree, and a brute-force algorithm based on routines in sklearn.metrics.pairwise. For our case, we used the brute-force algorithm using cosine similarity due to its fast computation for small datasets.

The application is built using the FastAPI framework, which allows for the creation of fast and efficient web APIs. When a user makes a request to the API (user data,nutrition data...) the model is used to generate a list of recommended food similar/suitable to his request (data) which are then returned to the user via the API.

The application's front-end is made with Streamlit. Streamlit is an open source app framework in Python language. It helps to create web apps for data science and machine learning in a short time. It is compatible with major Python libraries such as scikit-learn, Keras, PyTorch, SymPy(latex), NumPy, pandas, Matplotlib etc. For our case the front-end is composed of three web pages. The main page is Hello.py which is a welcoming page used to introduce you to my project. The side bar on the left allows the user to navigate too the smart recommendation page and the custom recommendation page. In the diet recommendation page the user can fill information about his age,weight,height.. and gets a diet recommendation based on his information. Besides, the custom food recommendation allows the user to specify more his food preferency using nutritional values.

# Deployement using Docker

**Why Docker?**

By using Docker, you can ensure that the environment in which the application is exactly the same as the environment in which it was built, which can help prevent unexpected issues and improve model performance. Additionally, Docker allows for easy scaling and management of the deployment, making it a great choice for larger machine learning projects.

**Docker-Compose**
Our project consist of different services (frontend,API). Therefore, our application should run on multiple containers. With the help of Docker-compose we can share our application using the yaml file that define the services that runs together.

# Technology Used

The project is created with:

- Python: 3.10.8
- fastapi 0.88.0
- uvicorn 0.20.0
- scikit-learn 1.1.3
- Pandas: 1.5.1
- Streamlit: 1.16.0
- streamlit-echarts 1.24.1
- Numpy: 1.21.5
- beautifulsoup4 4.11.1

# Conflict of Interest Statement:

This project has been developed for the sole purpose of research and development (R&D) learning. It is important to note that the individuals involved in this project may have a vested interest in the knowledge acquisition and skill development associated with the R&D process.

This project is not intended for high end commercial use, and its outcomes are primarily focused on POC Standard. The development team recognizes the potential for bias in the interpretation and reporting of results, given their direct involvement in the learning process. However, every effort has been made to maintain objectivity and integrity throughout the project.

Any unintended implications or potential conflicts arising from the development of this project are unintentional, and the team is committed to addressing them transparently. This disclosure is made to ensure openness and to provide context for the project's purpose.

# Developement Team:

- Prateek Dutta  (Machine learning Engineer, Hyderabad-India)
- Chetna Tambushkar (Data Science Engineer, Nagpur-India)

<h1>Securing a REST API with Flask Via Authentication and Authorization Project</h1>

<p>In this homelab we will secure REST APIs with Flask via Authentication and Authorization.</p>

<p>To begin we will install Flask via <code>pip install flask_httpauth</code>.</p>

![image alt](https://github.com/seanguevaraflood/RESTAPI/blob/4ece5f73a4750818325c3804e4b444309afe35c2/images/Flask%20Install.png
)

<p>We have our standard code that outlines and creates the sample data and defines a route via <code>/student</code> role.</p>

![image alt](https://github.com/seanguevaraflood/RESTAPI/blob/4ece5f73a4750818325c3804e4b444309afe35c2/images/HTTP%20Authentication.png
)

<p>Let’s add to this code with HTTP basic authentication.</p>

![image alt](https://github.com/seanguevaraflood/RESTAPI/blob/d1d4f0945c5879deda15ff1cb6e0e476faac2e6b/images/HTTP%20Authentication%202.png
)

<p>Next, let’s define a dictionary for a valid username and password for this example, as well as using <code>auth.verify_password</code> to define a valid username and password.</p>

![image alt](https://github.com/seanguevaraflood/RESTAPI/blob/d1d4f0945c5879deda15ff1cb6e0e476faac2e6b/images/HTTP%20Verification%201.png
)

<p>This function basically checks if both the username and password are correct; if they are, the username is returned.</p>

![image alt](https://github.com/seanguevaraflood/RESTAPI/blob/d1d4f0945c5879deda15ff1cb6e0e476faac2e6b/images/HTTP%20Verification%202.png
)

![image alt](https://github.com/seanguevaraflood/RESTAPI/blob/d1d4f0945c5879deda15ff1cb6e0e476faac2e6b/images/HTTP%20Verification%203.png
)

<p>This code returns a JSON response with all student records. It then requires authentication with a valid username and password. The <code>roll_no</code> also allows you to return a specific student based on the roll number.</p>

![image alt](https://github.com/seanguevaraflood/RESTAPI/blob/d1d4f0945c5879deda15ff1cb6e0e476faac2e6b/images/JSON%20Response.png
)

<p>We also programmed the root route to return <code>'Hello World!'</code>.</p>

![image alt](https://github.com/seanguevaraflood/RESTAPI/blob/d1d4f0945c5879deda15ff1cb6e0e476faac2e6b/images/JSON%20Reponse%20Code%20Hello%20World.png
)

<p>Here is the JSON result of a successful login.</p>

![image alt](https://github.com/seanguevaraflood/RESTAPI/blob/d1d4f0945c5879deda15ff1cb6e0e476faac2e6b/images/JSON%20Response%201.png
)

![image alt](https://github.com/seanguevaraflood/RESTAPI/blob/d1d4f0945c5879deda15ff1cb6e0e476faac2e6b/images/JSON%20Response%201.png
)

<p>Let’s also return a <code>Hello, (current user's username)</code> after a successful login.</p>

![image alt](https://github.com/seanguevaraflood/RESTAPI/blob/d1d4f0945c5879deda15ff1cb6e0e476faac2e6b/images/JSON%20Response%202.png
)

<p>Perfect, it works as it should! This concludes our homelab.</p>

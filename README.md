<h1>Securing a REST API with Flask Via Authentication and Authorization Project</h1>

<p>In this homelab we will secure REST APIs with Flask via Authentication and Authorization.</p>

<p>To begin we will install Flask via <code>pip install flask_httpauth</code>.</p>

<p>We have our standard code that outlines and creates the sample data and defines a route via <code>/student</code> role.</p>

<p>Let’s add to this code with HTTP basic authentication.</p>

<p>Next, let’s define a dictionary for a valid username and password for this example, as well as using <code>auth.verify_password</code> to define a valid username and password.</p>

<p>This function basically checks if both the username and password are correct; if they are, the username is returned.</p>

<p>This code returns a JSON response with all student records. It then requires authentication with a valid username and password. The <code>roll_no</code> also allows you to return a specific student based on the roll number.</p>

<p>We also programmed the root route to return <code>'Hello World!'</code>.</p>

<p>Here is the JSON result of a successful login.</p>

<p>Let’s also return a <code>Hello, (current user's username)</code> after a successful login.</p>

<p>Perfect, it works as it should! This concludes our homelab.</p>

<hr/>

<p>In this lab I will install and configure Nessus Essentials to perform credentialed vulnerability scans on Windows 10 Hosts. Implemented Vulnerability Management Function on sandbox networks.</p>

<p>Followed steps in the vulnerability response process: Discover, Prioritize, Assess, Report, Remediate, and Verify.</p>

<p>Conducted vulnerability assessments with Nessus and remediated vulnerabilities.</p>

<p>Developed automated remediation processes and procedures to mitigate problems in the future.</p>

<p>We started by downloading the Windows 10 ISO.</p>

<p>Now that we have the Windows 10 ISO installed, let's set up our Windows 10 virtual machine.</p>

<p>We are going to choose a bridged configuration so it can share the same network configurations as the host machine, making it accessible to our vulnerability scanner.</p>

<p>Great, now we have our virtual machine set up.</p>

<p>Great, now we have Nessus downloaded. Let's log in and set up our vulnerability scanner we will be using.</p>

<p>Now we have the VM and Nessus Essentials set up.</p>

<p>We will start with a basic scan before a credentialed scan.</p>

<p>Let’s get the IP address from the VM using <code>ipconfig</code>.</p>

<p>Now let’s try and ping the IP address with <code>ping [IP Address] -t</code>.</p>

<p>Unfortunately, it timed out so we need to disable the firewall on the virtual machine.</p>

<p>Great, now that we have turned the firewalls off, we are getting a reply from the VM.</p>

<p>Let’s now run a basic scan from Nessus.</p>

<p>Looking at the uncredentialed scan, we don’t have too many serious vulnerabilities seen. Now let’s compare a credentialed scan with the uncredentialed scan. To do this, we need to enable Remote Registry in Windows Services. This will allow the VM to accept credentialed scans from Nessus as long as we provide the correct information to both.</p>

<p>We also have to disable the User Account Control.</p>

<p>Now we have to go into the registry and further disable User Account Control by adding a key.</p>

<p>Now that we have the virtual machine’s settings optimized for this credentialed scan, let’s put in our login credentials into Nessus.</p>

<p>Now let’s run the credentialed scan and compare it to the uncredentialed scan.</p>

<p>Wow, this is very different from our uncredentialed scan.</p>

<p>A lot of these could be fixed by automatic patching.</p>

<p>Now let’s download a deprecated version of Firefox.</p>

<p>Now that we have downloaded the old version of Firefox, let’s see how our Nessus scan changes.</p>

<p>Wow, it has resulted in a lot of critical vulnerabilities.</p>

<p>It just goes to show you how important patching is.</p>

<p>As a final scan, let’s uninstall the deprecated Firefox and fully update Windows to its current version.</p>

<p>Great! The updates and removal of deprecated software have helped us get rid of a lot of previously existing vulnerabilities. There are a few left, but with careful analysis, we could get rid of all the critical vulnerabilities. We could optimize and automate this process for better security for a large organization.</p>

<p>This concludes our Vulnerability Management Homelab.</p>

# DevOps Engineer Challenge @ Pocketful

## Mission

The mission of this challenge is to set up a basic web server using Nginx on a localhost environment. The focus is on configuring Nginx to serve static HTML pages, including a main page and a secondary page accessible via a specific path (/yellow).

## Tasks

### 1. Install Nginx Locally
{NOTE: I don't have VM in my system so took help of AWS cloud }

1. Lunched the EC2 instance with amazone linux
2. Add inbound rule in Security group to start port 22 and port 80
3. Now take SSH or our linux machin on our local mobaxtrim
4. Now with help of SSH we are in our EC2 instance
5. Now update the system "sudo yum update -y"
6. Install Nginx " sudo yum install nginx "
7. Start Nginx "sudo systemctl start nginx"
8. Enable Nginx "sudo systemctl enable nginx"

### 2. Create Static HTML Pages

Design simple HTML pages to serve as follows:

#### Home Page (index.html)

Content: "Welcome to my Nginx server! My name is PAWAN."

#### Yellow Page (yellow.html)

Content: "This is the yellow page. It's distinct from the home page."

### 3. Configure Nginx

Edit the Nginx configuration file to

- move index.html and yellow.html in location usr/share/nginx/html/.

### 4. Testing the Setup

After configuration:

- Restart Nginx.
- Test both pages.
- Ensure both the main page and /yellow path are correctly served by Nginx.

## Hints n' Cues

### Nginx Configuration

- The configuration file is typically located at `/etc/nginx/nginx.conf`if it is Ububtu distribution
- And configuration file is typically located at /usr/local/nginx/conf/nginx.conf`if it is redhat linux distribution
- Use `location /` for the root and `location /yellow` for the secondary path.
- The `root` directive in Nginx is used to specify the directory where the HTML files are located.

### HTML Page Creation

- the simple HTML; focus on differentiating the home page and /yellow page.
- Ensure the HTML files are placed in the directory specified in the Nginx configuration.

### Testing

- Access http://localhost or (EC2 instance public IP) and http://localhost/yellow.html  (EC2 instance public IP)/yellow.html in your browser to test.
- Check for any errors and ensure that Nginx serves the correct pages.

## Test Data

#### Home Page (index.html):

Content: "Welcome to my Nginx server! My name is PAWAN."

#### Yellow Page (yellow.html):

Content: "This is the yellow page. It's distinct from the home page."


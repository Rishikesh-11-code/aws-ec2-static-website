# AWS EC2 Static Website Hosting with Apache

## Project Overview

A custom-designed static website hosted on an AWS EC2 Linux instance using Apache HTTP Server.

This project demonstrates practical cloud computing, Linux administration, basic networking, and website deployment.

## Architecture

Browser → AWS Security Group → EC2 Instance → Apache HTTP Server → `index.html`

## Technologies Used

- AWS EC2
- Amazon Linux 2023
- Apache HTTP Server
- Linux command line
- HTML5 and CSS3
- AWS Security Groups

## Deployment Steps

### 1. Launch EC2

Launch an Amazon Linux 2023 EC2 instance and configure a key pair.

### 2. Configure Security Groups

- Allow SSH (port 22) only from your IP address.
- Allow HTTP (port 80) for public website access.

### 3. Install Apache

```bash
sudo dnf update -y
sudo dnf install httpd -y
sudo systemctl enable --now httpd
```

### 4. Deploy the Website

Create the website file:

```bash
sudo nano /var/www/html/index.html
```

Paste the HTML and CSS code from `index.html` in this repository.

### 5. Verify Deployment

```bash
sudo systemctl status httpd
curl -I http://localhost
```

### 6. Access the Website

Open `http://YOUR-EC2-PUBLIC-IP` in your browser, replacing the placeholder with the instance's actual public IPv4 address.

## Project Features

- Custom website design
- Responsive page layout
- Technology stack section
- Cloud deployment workflow
- Apache-based static content hosting

## Skills Demonstrated

AWS EC2, Linux, Apache, HTML, CSS, SSH, Security Groups, troubleshooting, and technical documentation.

## Future Improvements

- Automate setup with Bash
- Provision infrastructure using Terraform
- Add CI/CD using GitHub Actions
- Configure HTTPS

## Author

Rishikesh Dapse

Computer Engineering Student | Aspiring Cloud & DevOps Engineer

## Disclaimer

This is an educational project. AWS resources may incur charges. Review your AWS billing and terminate resources when no longer needed.

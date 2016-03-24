FROM centos

# Update ec2 instance
RUN yum update -y

# Install Node.js and npm
RUN     curl --silent --location https://rpm.nodesource.com/setup_5.x | bash -
RUN     yum install -y nodejs 5.5
# Install Git
# RUN yum groupinstall -y "Development Tools" (super big complete dev tools)

RUN yum install -y git
RUN yum install -y gettext-devel openssl-devel perl-CPAN perl-devel zlib-devel
RUN yum install -y wget
RUN yum install -y make
RUN yum install -y tar

# Make dir for our app
RUN	mkdir app

# Install app dependencies
COPY package.json /app/package.json
RUN cd /app; npm install

# Bundle app source
COPY . /app

# Get forever
RUN  npm install -g karma-cli
RUN  npm install -g karma
RUN  npm install -g forever

EXPOSE  8080

CMD ["node --version"]
CMD ["npm --version"]
CMD ["git -version"]
CMD ["node", "/app/index.js"]

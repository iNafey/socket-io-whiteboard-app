# Distributed Whiteboard app

This project is a distributed whiteboard app created using React (front-end) and Node & Express (backend) with a Redis database to store the whiteboard state. This was then deployed on a private cloud. AWS Elastic Kubernetes Service (EKS) was used to create a Kubernetes cluster with 2 worker nodes. The dockerized multi-container app (one each for front-end and back-end) was then deployed on the Kubernetes cluster using a helm chart.

## Requirements

Node & NPM

## Instructions on running the app

### Frontend

ReactJS frontend located under `app/src/`

To install on first download/setup run `npm install`
To start go to the react directory and run `npm run dev`

### Backend

Express, SocketIO and Redis under `server/`

To install on first download/setup run `npm install`
To start go to server directory and run `node .`

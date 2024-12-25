# Instructions for Running the ToDo App Docker Container

## 1. Docker Hub Repository Link

You can find the Docker image for the ToDo app in my personal Docker Hub repository here:

[My Docker Hub Repository - todoapp](https://hub.docker.com/r/srtrace/py-todo-app)

## 2. Build the Docker Image

To build the Docker image for the ToDo app, follow these steps:

1. Clone or download the project to your local machine.
2. Open the terminal/command prompt and navigate to the directory where the `Dockerfile` is located.
3. Run the following command to build the Docker image:

   ```bash
   docker pull srtrace/py-todo-app .
   ```

This will create a Docker image with the tag `todoapp:1.0.0`.

## 3. Push the Docker Image to Docker Hub

Once the image is built, you can upload it to Docker Hub.

1. Tag the image with your Docker Hub username:

   ```bash
   docker tag todoapp:1.0.0 <your-dockerhub-username>/todoapp:1.0.0
   ```

   Replace `<your-dockerhub-username>` with your actual Docker Hub username.

2. Push the image to Docker Hub:

   ```bash
   docker push <your-dockerhub-username>/todoapp:1.0.0
   ```

This will upload your image to your Docker Hub repository.

## 4. Run the Docker Container

To run the ToDo app container locally:

1. Use the following command to run the Docker container:

   ```bash
   docker run -p 8080:8080 <your-dockerhub-username>/todoapp:1.0.0
   ```

   This will run the container and expose port `8080` to your local machine.

## 5. Access the Application

After the container is running, open your web browser and navigate to the following URL: http://localhost:8080

You should now see the ToDo app running locally in your browser.

## 6. Troubleshooting

If you encounter any issues, try the following:

- **If the container does not start**: Check the logs of the container using the command:

  ```bash
  docker logs <container_id>
  ```

- **If the Docker build fails**: Ensure that you are in the correct directory and that the `Dockerfile` is properly configured.

## 7. Create Pull Request

Once you've added or updated your `INSTRUCTION.md` file, commit your changes and create a pull request (PR) for validation. This can be done through your GitHub repository interface:

1. Commit your changes with a message like "Add instructions for building and running Docker container."
2. Open your repository in GitHub and create a pull request.
3. Attach the PR to the platform for validation.

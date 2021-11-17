# RazorPagesPizza
https://docs.microsoft.com/en-us/learn/modules/create-razor-pages-aspnet-core/1-introduction

## Running the asp.net core app
Simply run the app with `dotnet run`.
Run the app with hot reload by typing `dotnet watch`.

## Running the app inside a Docker container
The `Dockerfile` specifies to build and run the app on top of the [dotnet sdk docker image](https://hub.docker.com/_/microsoft-dotnet-sdk).
Build and launch the docker container by typing

```
docker build -t razorpagespizza .
docker run -it -p 5000:80 razorpagespizza
```

This `-p 5000:80` maps the container's port 80 to your localhost's port 5000.
Finally you can access the website on `localhost:5000`.

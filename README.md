# RazorPagesPizza
In order to get familiar with razor pages and asp.net core apps, I've followed this [tutorial](https://docs.microsoft.com/en-us/learn/modules/create-razor-pages-aspnet-core/1-introduction
), which was also very nicely done by Scott Hanselmann and Maira Wenzel in this [video session](https://www.youtube.com/watch?v=YnU1FckB2s4) .


I've extended this app to be run from inside a docker container, as in this [example](https://docs.microsoft.com/de-de/aspnet/core/host-and-deploy/docker/building-net-docker-images?view=aspnetcore-6.0) for creating and running docker images for asp.net core.

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

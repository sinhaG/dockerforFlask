# dockerforFlask


# How to use

We are leveraging the code base mentioned here - https://github.com/sinhaG/Heroku-Flask-ModelV1


<ul>
  <li>Checkout the branch with the docker file.</li>
  <li> use the below command to building docker image. Here in the example <h3>"modelv1" is the "Name" you want to give to you docker </h3>
    <p>
docker build -t modelv1:latest .
      </p></li>
  <li>use the command to rune the file on you terminal
  <p>
    docker run --rm -it --network=host -p 5000:5000 modelv1
    </p>
   
  </li>
</ul>

Once the docker image is created you can deploy to heroku using following commands.<h3>"flaskrestmodel" is the "Name" you want to give to you heroku application </h3>

<ul>
  <li>heroku login</li>
<li>heroku container:login</li>
<li>heroku container:push web --app flaskrestmodel</li>
<li>heroku container:release web --app flaskrestmodel</li>
<li>heroku open --app flaskrestmodel</li>
</ul>

# A script for API stress testing:
The original code came from [here](https://medium.com/@mnu/run-multiple-postman-collection-in-parallel-stress-ee20801922ed).

## Instalation

Build:
```docker-compose build```

Create a container:
```docker-compose run --rm node```

Check container name:
```docker ps```

Enter the container:
```docker exec -it {container_name} bash```

## Running

Let your postman collection inside postman folder.

For parallel requests set the constant `PARALLEL_RUN_COUNT` inside *index.js* and run:
```npm start > out.txt```

For Sequential tests, call newman tool directly. Here is a sample:
```newman run postman/stonebankcoll.json -n 10000 > out.txt```

Check the result in your `out.txt`
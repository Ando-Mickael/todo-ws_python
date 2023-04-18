# TODO Backend App using Django Rest Framework

This project is a simple TODO backend app built using Django Rest Framework (DRF) created by **Informa'Tiako** which provides a RESTful API for managing tasks.

## Installation

1.  Clone the repository:

```bash
git clone https://github.com/your_username/todo-backend.git
```

2.  Install the required packages:


```bash
pip install -r requirements.txt
```

3.  Migrate the database:


```bash
python manage.py migrate
```

4.  Run the server:


```bash
python manage.py runserver
```

## API Endpoints

- ``` GET /api/tasks/``` - Retrieve all tasks
- ``` POST /api/tasks/``` - Create a new task
- ``` GET /api/tasks/<int:pk>/``` - Retrieve a specific task
- ``` PUT /api/tasks/<int:pk>/``` - Update a specific task
- ``` DELETE /api/tasks/<int:pk>/``` - Delete a specific task

## Request and Response Formats

### Task


```bash
``{     "id": 1,     "title": "Task Title",     "description": "Task Description",     "completed": false,     "created_at": "2023-04-18T12:00:00Z",     "updated_at": "2023-04-18T12:00:00Z" }``
```

### Request


```bash
``{     "title": "Task Title",     "description": "Task Description",     "completed": false }``
```

### Response


```bash
``{     "id": 1,     "title": "Task Title",     "description": "Task Description",     "completed": false,     "created_at": "2023-04-18T12:00:00Z",     "updated_at": "2023-04-18T12:00:00Z" }``
```

## Authentication

This project uses Token-based authentication. To access the API endpoints, you need to first obtain a token by sending a ```POST``` request to the ```/api/token/``` endpoint with your credentials in the request body. Once you obtain a token, you can include it in the ```Authorization``` header of subsequent requests to authenticate yourse
lf.

## Testing

To run the tests:


```bash
python manage.py test
```

## Contribution

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
Informa'Tiako - 
[MIT](https://choosealicense.com/licenses/mit/)
## Testing and Database Management

1. **Explore the API**: Use the Swagger UI at `http://localhost/docs` to familiarize yourself with the API endpoints, request/response formats, and authentication mechanisms. Swagger UI provides an interactive interface to explore and test the API endpoints.

2. **Run Tests**: Execute the provided test suite using pytest, a popular testing framework for Python. Running tests ensures that the existing functionality of the API is working as expected. Note that running tests will drop the database tables, so you may need to manually drop the Alembic version table using PGAdmin and re-run migrations to ensure a clean state.

3. **Increase Test Coverage**: To enhance the reliability of the API, aim to increase the project's test coverage to 90%. Write additional tests for various scenarios and edge cases to ensure that the API handles different situations correctly.

## Collaborative Development Using Git

1. **Enable Issue Tracking**: Enable GitHub issues in your repository settings. [GitHub Issues](https://guides.github.com/features/issues/) is a powerful tool for tracking bugs, enhancements, and other tasks related to the project. It allows you to create, assign, and prioritize issues, facilitating effective collaboration among team members.

2. **Create Branches**: For each issue or task you work on, create a new branch with a descriptive name using the `git checkout -b` command. Branching allows you to work on different features or fixes independently without affecting the main codebase. It enables parallel development and helps maintain a stable main branch.

3. **Pull Requests and Code Reviews**: When you have completed work on an issue, create a [pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests) to merge your changes into the main branch. Pull requests provide an opportunity for code review, where your team members can examine your changes, provide feedback, and suggest improvements. Code reviews help maintain code quality, catch potential issues, and promote knowledge sharing among the team.

## Specific Issues to Address

In this assignment, you will identify, document, and resolve five specific issues related to:

1. **Username validation**: Investigate and resolve any issues related to username validation. This may involve handling special characters, enforcing length constraints, or ensuring uniqueness. Proper username validation is essential to maintain data integrity and prevent potential security vulnerabilities.

2. **Password validation**: Ensure that password validation follows security best practices, such as enforcing minimum length, requiring complexity (e.g., a mix of uppercase, lowercase, numbers, and special characters), and properly hashing passwords before storing them in the database. Robust password validation protects user accounts and mitigates the risk of unauthorized access.

3. **Profile field edge cases**: Test and handle various scenarios related to updating profile fields. This may include updating the bio and profile picture URL simultaneously or individually. Consider different combinations of fields being updated and ensure that the API handles these cases gracefully. Edge case testing helps uncover potential issues and ensures a smooth user experience.

Additionally, you will resolve a sixth issue demonstrated in the instructor video. These issues will test various combinations and scenarios to simulate real-world usage and potential edge cases. By addressing these specific issues, you will gain experience in identifying and resolving common challenges in API development.

## Latest Docker Image:
https://hub.docker.com/repository/docker/hallsamir14/is421event_manager-fastapi

## Resources and Documentation

- **Instructor Videos and Important Links**:
 - [Introduction to REST API with Postgres](https://youtu.be/dgMCSND2FQw) - This video provides an overview of the REST API you'll be working with, including its structure, endpoints, and interaction with the PostgreSQL database.
 - [Assignment Instructions](https://youtu.be/TFblm7QrF6o) - Detailed instructions on your tasks, guiding you through the assignment step by step.
 - [Git Command Reference I created and some explanation for collaboration with git](git.md)
 - [Docker Commands and Running The Tests in the Application](docker.md)
 - Look at the code comments:
    - [Test Configuration and Fixtures](tests/conftest.py)
    - [API User Routes](app/routers/user_routes.py)
    - [API Oauth Routes - Connection to HTTP](app/routers/oauth.py)
    - [User Service - Business Logic - This implements whats called the service repository pattern](app/services/user_service.py)
    - [User Schema - Pydantic models](app/schemas/user_schemas.py)
    - [User Model - SQl Alchemy Model ](app/models/user_model.py)
    - [Alembic Migration - this is what runs to create the tables when you do alembic upgrade head](alembic/versions/628adcb2d60e_initial_migration.py)
    - See the tests folder for all the tests

 - API Documentation: `http://localhost/docs` - The Swagger UI documentation for the API, providing information on endpoints, request/response formats, and authentication.
 - Database Management: `http://localhost:5050` - The PGAdmin interface for managing the PostgreSQL database, allowing you to view and manipulate the database tables.

- **Additional Resources**:
 - [SQLAlchemy Library](https://www.sqlalchemy.org/) - SQLAlchemy is a powerful SQL toolkit and Object-Relational Mapping (ORM) library for Python. It provides a set of tools for interacting with databases, including query building, database schema management, and data serialization. Familiarize yourself with SQLAlchemy's documentation to understand how it is used in the project for database operations.
 - [Pydantic Documentation](https://docs.pydantic.dev/latest/) - Pydantic is a data validation and settings management library for Python. It allows you to define data models with type annotations and provides automatic validation, serialization, and deserialization. Consult the Pydantic documentation to understand how it is used in the project for request/response validation and serialization.
 - [FastAPI Framework](https://fastapi.tiangolo.com/) - FastAPI is a modern, fast (high-performance) Python web framework for building APIs. It leverages Python's type hints and provides automatic API documentation, request/response validation, and easy integration with other libraries. Explore the FastAPI documentation to gain a deeper understanding of its features and how it is used in the project.
 - [Alembic Documentation](https://alembic.sqlalchemy.org/en/latest/index.html) - Alembic is a lightweight database migration tool for usage with SQLAlchemy. It allows you to define and manage database schema changes over time, ensuring that the database structure remains consistent across different environments. Refer to the Alembic documentation to learn how to create and apply database migrations in the project.

These resources will provide you with a solid foundation to understand the tools, technologies, and concepts used in the project. Don't hesitate to explore them further and consult the documentation whenever you encounter challenges or need clarification.

## Conclusion

This assignment is designed to challenge you, help you grow as a developer, and prepare you for the real-world responsibilities of a Software QA Analyst/Developer. By working on realistic issues, collaborating with your team, and focusing on testing and quality assurance, you will gain valuable experience that will serve you throughout your career.

Remember, the goal is not just to complete the assignment but to embrace the learning journey. Take the time to understand the codebase, ask questions, and explore new concepts. Engage with your team members, seek feedback, and learn from their experiences. Your dedication, curiosity, and willingness to learn will be the key to your success in this role.

We are excited to have you on board and look forward to seeing your contributions to the project. Your fresh perspective and skills will undoubtedly make a positive impact on our team and the quality of our software.

If you have any questions or need assistance, don't hesitate to reach out to your mentor or team lead. We are here to support you and ensure that you have a rewarding and enriching experience.

Once again, welcome to the Event Manager Company! Let's embark on this exciting journey together and create something remarkable.

Happy coding and happy learning!
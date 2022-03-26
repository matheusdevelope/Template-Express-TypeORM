# Awesome Project Build with TypeORM

Steps to run this project:

1. Run `npm i` command
2. Setup database settings inside `data-source.ts` file
3. Run `npm start` command

4. The release of TypeORM 3.3 change method of CLI work, now we need pass the "-d path_of_datasource_file.ts" in some commands (migration:run, create, etc) all the methods tha needs acess the DB need the "-d" param.

5. To start create a database, put the connections on data-source file and run `npm run typeorm:starttables`, this will generate the migration file of entities on project then will execute the queryes on database.

6. The command above generate only one file with all schema of db, so, run this command more then one time with the old files in src/migration will throw a error because the schema already exists, to make new migrations and run, use `npm run typeorm:create` then `npm run typeorm:run`.

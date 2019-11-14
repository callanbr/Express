
sequelize init
sequelize-auto -h localhost -d auth -u root -x AVeryStrongPassword1! -o "./models" -t users


sequelize-auto -h localhost -d sakila -u root -x Password1! -o "./models" -t film,actor,film_actor


sequelize model:generate --name users --attributes UserId:integer,FirstName:string,LastName:string,Email:string,Username:string,Password:string
makemigration --name initial_migration
sequelize db:create
sequelize db:migrate
# Go-GraphQL-Example

## Installing
First create the folder:
```bash
mkdir go-graphql-example
go mod init <your-project-repo-uri>
```

Then install the dependencies:
```bash
printf '// +build tools\npackage tools\nimport (_ "github.com/99designs/gqlgen"\n _ "github.com/99designs/gqlgen/graphql/introspection")' | gofmt > tools.go
go mod tidy
```
Finally generate the playground and run:
```bash
go run github.com/99designs/gqlgen init
go run server.go
```

## Tips

Once you have your schema ready, you can generate the code you need from
typing 
```bash
go run github.com/99designs/gqlgen generate
```
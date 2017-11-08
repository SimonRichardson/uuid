# UUID

UUID (Universally Unique Identifier) is a simple package that implements V4 of
the UUID specification.

It also aims to make very basic assumptions of how a empty UUID behaves when 
used for verifying and checking for equality.

-----

There are few methods for creating a UUID, with or without a random, because
there are some environments that can not depend on the basic global random in
the standard library. Locking when generating a lot of ids can cause various 
issues and identify themselves when using `-race`.

```go
id, err := uuid.New()
if err != nil {
  panic(err)
}
fmt.Println(id.String())
```

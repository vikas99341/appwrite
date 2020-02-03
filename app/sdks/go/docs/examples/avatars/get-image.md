package main

import (
    "fmt"
    "github.com/appwrite/sdk-for-go"
)

func main() {
    var client := appwrite.Client{}

    client.SetProject("")
    client.SetKey("")

    var service := appwrite.Avatars{
        client: &client
    }

    var response, error := service.GetImage("https://example.com", 0, 0)

    if error != nil {
        panic(error)
    }

    fmt.Println(response)
}
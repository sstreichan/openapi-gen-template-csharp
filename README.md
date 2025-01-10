# Custom OpenAPI Generator Template for C#

This repository contains a custom template for the OpenAPI Generator to generate C# client code. The template includes customized `.csproj` file settings and Mustache templates for API and model classes.

## Requirements

- [OpenAPI Generator](https://openapi-generator.tech/)
- [.NET 6.0 SDK](https://dotnet.microsoft.com/download/dotnet/6.0)

## Files

- `MyCustomTemplate.csproj`: The main project file for the custom template.
- `service.yaml`: The OpenAPI service definition file with custom metadata.
- `templates/csharp/api.mustache`: The Mustache template for generating API classes.
- `templates/csharp/model.mustache`: The Mustache template for generating model classes.
- `templates/csharp/project.mustache`: The Mustache template for generating the `.csproj` file.

## Setup

1. **Install OpenAPI Generator**:
   Follow the instructions on the [OpenAPI Generator website](https://openapi-generator.tech/docs/installation) to install the OpenAPI Generator.

2. **Install .NET 6.0 SDK**:
   Download and install the [.NET 6.0 SDK](https://dotnet.microsoft.com/download/dotnet/6.0).

## Usage

1. **Prepare Your OpenAPI Definition**:
   Ensure your OpenAPI definition file (`service.yaml`) is correctly set up with the necessary metadata values.

2. **Generate the Client Code**:
   Use the OpenAPI Generator to generate the client code with the custom template. Run the following command:

   ```sh
   openapi-generator-cli generate -i service.yaml -g csharp -t templates/csharp -o output/directory
   ```

   Replace `output/directory` with the path where you want to generate the client code.

3. **Build the Project**:
   Navigate to the generated project directory and build the project using the .NET CLI:

   ```sh
   dotnet build
   ```

4. **Run the Project**:
   After building the project, you can run it using the following command:

   ```sh
   dotnet run
   ```

## Custom Metadata

The `service.yaml` file includes custom metadata values that are used to populate the `.csproj` file. Ensure that the following metadata values are included in your `service.yaml` file:

- `title`
- `description`
- `termsOfService`
- `contact` (email and url)
- `license` (name and url)
- `x-authors`
- `x-company`
- `x-assemblyTitle`

## License

This project is licensed under the [sense.ai.tion license](https://senseaition.com/terms/).

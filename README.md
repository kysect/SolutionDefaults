# Kysect.SolutionDefaults

![NuGet](https://img.shields.io/nuget/v/Kysect.SolutionDefaults.svg)

## Idea

The idea behind Kysect.SolutionDefaults is to provide a set of default settings for new projects and up-to-date them using NuGet packages. NuGet maintainers can update the settings and the users will get the updates when they update the package.

List of settings that can be provided by Kysect.SolutionDefaults:

- .editorconfig
- Default icon of Kysect projects
- Kysect.SolutionDefaults.props file with default settings for new projects

## Configuration

Package provide a set of MSBuild properties that can be used to configure the behavior of the package:

- `SolutionDefaultsUseMetadataOptions` - if set to `true` the package will use Kysect metadata options for the project (author, company, copyright)
- `SolutionDefaultsUseLicense` - if set to `true` the package will use MIT license for the project
- `SolutionDefaultsUseAnalyzersOptions` - if set to `true` the package will enable Roslyn analyzers for the project (enable NRT, Roslyn analyzers and treat warnings as errors)
- `SolutionDefaultsUseBuildOptions` - if set to `true` the package will use Kysect build options for the project (latest language version, artifacts output, implicit `using` directives)
- `SolutionDefaultsUsePublishOptions` - if set to `true` the package will use Kysect publish options for the project (RepositoryType, deterministic build, `.snupkg` symbols)
- `SolutionDefaultsCopyEditorConfig` - if set to `true` the package will copy `.editorconfig` file to the solution directory
- `SolutionDefaultsUseIcon` - if set to `true` the package will use Kysect icon for the project
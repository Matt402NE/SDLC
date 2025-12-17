# # (Draft) Static Code Analysis (SCA)

Static code analysis for .NET  uses the same built-in mechanisms, primarily the Roslyn analyzers, to give developers compile time feedback. Code analysis is enabled by default for projects targeting .NET 5 or later.

## How it works in .NET 

The .NET SDK includes a set of Roslyn analyzers that inspect your C# or Visual Basic code for quality, style, and security issues without running the application. 

- **Enabled by Default**: If your project file (`.csproj`) specifies a `TargetFramework` of `net10.0` (or `net5.0` and later), the built-in analyzers are automatically active during the build process and in the Visual Studio Error List.
- **Integration**: Analysis can be run manually in Visual Studio, or automatically as part of your build and Continuous Integration (CI) pipeline.
- **Configuration**: You can customize the analysis rules using project properties in your `.csproj` file or a centralized `Directory.Build.props` file. 

## Key Configuration Properties

These properties help tailor the analysis to your team's standards: 

- **`AnalysisLevel`**: Specifies which rules to enable. The default value is `latest`, ensuring you use the most current analyzers available with the SDK.
- **`EnforceCodeStyleInBuild`**: Set to `true` to enable code-style warnings (*IDExxxx* rules) during the build process, not just in the IDE.
- **`TreatWarningsAsErrors`**: Set this to `true` to fail the build if any warning (including analyzer warnings) is detected. A more specific property is `CodeAnalysisTreatWarningsAsErrors`, which only treats code quality warnings (*CAxxxx* rules) as errors. 









Additional Tools

While the built-in analyzers offer strong foundational support, various third-party tools provide more advanced features, particularly for security (SAST) and complex data flow analysis: 

- **SonarQube/SonarCloud**: A popular platform for continuous code quality inspection that integrates deeply into CI/CD pipelines.
- **Snyk**: A developer security platform that identifies vulnerabilities in custom code and open-source dependencies (SCA).
- **CodeQL**: A semantic code analysis engine used for finding security vulnerabilities through data flow visualization.





These tools examine your code for general security flaws and vulnerabilities (e.g., OWASP Top 10 issues). 

- **Security Code Scan**: A set of Roslyn analyzers for C# and VB.NET that flags security vulnerabilities directly in your IDE as you code and during builds.
- **SonarQube/SonarLint**: SonarQube is an enterprise-grade platform for continuous code quality inspection, while SonarLint provides real-time feedback within your IDE.
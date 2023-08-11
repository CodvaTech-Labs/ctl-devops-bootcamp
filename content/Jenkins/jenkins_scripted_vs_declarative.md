+++
title = "Jenkins Scripted Vs Declarataive"
weight = 25
chapter = false
pre = "<b> 1.9 </b>"
+++

Here's a comparison of Jenkins Scripted Pipeline and Declarative Pipeline in a table format:

| Feature                  | Scripted Pipeline                              | Declarative Pipeline                          |
|--------------------------|-----------------------------------------------|----------------------------------------------|
| Syntax Approach         | Groovy scripting with full flexibility       | Predefined structured syntax                |
| Stages and Steps        | Define using custom Groovy scripting         | Define using predefined directives         |
| Agent Configuration     | `node` or `docker` blocks for agent selection| `agent` directive for agent configuration  |
| Environment Variables  | Custom Groovy code for environment variables | `environment` directive                    |
| Conditional Execution   | Full Groovy control using `if`, `switch`, etc.| `when` directive for conditional execution |
| Post-Build Actions      | Use Groovy scripting for post-build actions | `post` directive for post-build actions     |
| Parallel Execution      | Custom scripting using `parallel` step       | Not directly supported (limited parallel)  |
| Custom Libraries/Steps  | Custom functions, libraries, and shared steps| Limited support for custom shared libraries|
| Error Handling         | Use try-catch blocks for error handling     | Limited error handling options              |
| Ease of Use            | More complex due to scripting requirements | Simpler, structured syntax                 |
| Extensibility          | Highly extensible with full Groovy scripting| Limited extensibility beyond predefined    |
| Code Reusability       | Requires coding custom functions/libraries | Simplified reuse through predefined syntax |
| Suitable For           | Advanced users, complex and custom pipelines| Users looking for simplicity and structure  |

Keep in mind that the choice between Scripted and Declarative Pipeline depends on your team's requirements, familiarity with Groovy scripting, complexity of the pipeline, and the need for customization. Declarative Pipeline is often recommended for simpler pipelines, while Scripted Pipeline offers greater flexibility and control for more intricate and customized build processes.
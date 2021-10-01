# Exein analyzer CLI


## Getting started
### Usage

```bash
efa [command] [arguments]
```

### How to build
  
Development environment:  
```bash
cargo build --no-default-features --features "development"
```

Staging environment:  
```bash
cargo build --no-default-features --features "staging"
```

Release (AWS) environment:
```bash
cargo build --release
```

### How to package

1. Install makeself
2. Make executable the release script:
    ```bash
    chmod +x package-release.sh
    ```
3. Launch the script:
    ```bash
    ./package-release.sh
    ```


## Examples

- List personal projects: `$ efa list` or `$ efa ls`
- Create a new analysis:  `$ efa create -f <fw-path> -t <fw-type> -n <project-name>` or `$ efa new -f <fw-path> -t <fw-type> -n <project-name>`
- View project results overview: `$ efa overview -i <uuid-project>` or `$ efa show -i <uuid-project>`
- View analysis results: `$ efa analysis -i <uuid-project> -a PeimDxe`
- Delete project: `$ efa delete -i <uuid-project>` or `$ efa rm -i <uuid-project>`
- Log out: `$ efa logout`
- Create an API key: `$ efa apikey -a create`
- List API key: `$ efa apikey -a list`
- Delete API key: `$ efa apikey -a delete`
- Save PDF report: `$ efa report -i <uuid-project>`


## Features

- [x] List projects
- [x] Get project overview
- [x] Delete project
- [x] Create project
- [x] Logout
- [x] Get analyses
- [x] API key
 
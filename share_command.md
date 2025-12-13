# Share Command

Copy and paste the following function into your terminal (zsh) to enable the `share_link` command.

```zsh
share_link() {
    local file="$1"
    # The base URL for your GitHub Pages site
    local base_url="https://hoyongj.github.io/a4fc36d8-e9d2-4350-a32b-0c7762f410f3"
    
    if [[ ! -f "$file" ]]; then
        echo "File not found: $file"
        return 1
    fi

    # Get relative path, removing leading ./ if present
    local rel_path="${file#./}"
    
    # Simple URL encoding for spaces
    local url_path="${rel_path// /%20}"
    
    local full_url="${base_url}/${url_path}"
    local name=$(basename "$file")
    
    # Check if link already exists in readme.md to avoid duplicates
    if grep -q "$full_url" readme.md; then
        echo "Link for $name already exists in readme.md"
    else
        # Append the link to readme.md
        echo "- [$name]($full_url)" >> readme.md
        echo "Added $name to readme.md"
    fi
}
```

## Usage

### 1. Share a specific file
```zsh
share_link path/to/your/file.html
```

### 2. Automatically capture all HTML and PDF files (excluding libs)
This command finds all `.html` and `.pdf` files, excluding those in `libs` directories or hidden folders, and adds them to `readme.md`.

```zsh
find . \( -name "*.html" -o -name "*.pdf" \) -not -path "*/libs/*" -not -path "*/.*" | while read file; do share_link "$file"; done
```

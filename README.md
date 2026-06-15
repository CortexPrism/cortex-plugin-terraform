# cortex-plugin-terraform

Generate IaC from natural language, validate, plan, and apply with Terraform or Pulumi.

## Installation

```bash
cortex plugin install marketplace:cortex-plugin-terraform
cortex plugin install github:CortexPrism/cortex-plugin-terraform
cortex plugin install ./manifest.json
```

## Quick Start

```bash
cortex tools list
cortex chat --plugin cortex-plugin-terraform
```

## Tools

### iac_generate — Generate IaC from description
- `description` (string, required)
- `tool` (enum: terraform/pulumi, terraform)
- `provider` (string, aws)
- `output_file` (string, required)

### iac_validate — Validate IaC
- `path` (string, required)
- `tool` (string)

### iac_plan — Run plan/preview
- `path` (string, required)
- `tool` (string)

### iac_apply — Apply changes
- `path` (string, required)
- `tool` (string)
- `auto_approve` (boolean)

### iac_destroy — Destroy infrastructure
- `path` (string, required)
- `tool` (string)
- `force` (boolean)

## Configuration

```json
{
  "plugins": {
    "cortex-plugin-terraform": {
      "enabled": true,
      "config": {
        "defaultTool": "terraform",
        "defaultProvider": "aws",
        "requireApproval": true
      }
    }
  }
}
```

## Development

```bash
deno task test
deno task lint
deno task validate
```

## License

MIT

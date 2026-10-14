# terraform-github-repo

Manages Github repos

<!-- BEGIN_TF_DOCS -->
## Requirements

| Name | Version |
| ---- | ------- |
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.0.0 |
| <a name="requirement_github"></a> [github](#requirement\_github) | >= 4.20.0 |

## Providers

| Name | Version |
| ---- | ------- |
| <a name="provider_github"></a> [github](#provider\_github) | >= 4.20.0 |

## Modules

No modules.

## Resources

| Name | Type |
| ---- | ---- |
| [github_branch_default.default](https://registry.terraform.io/providers/integrations/github/latest/docs/resources/branch_default) | resource |
| [github_repository.repo](https://registry.terraform.io/providers/integrations/github/latest/docs/resources/repository) | resource |
| [github_branch.main](https://registry.terraform.io/providers/integrations/github/latest/docs/data-sources/branch) | data source |

## Inputs

| Name | Description | Type | Default | Required |
| ---- | ----------- | ---- | ------- | :------: |
| <a name="input_archived"></a> [archived](#input\_archived) | Set to true to archive the repository (read-only on GitHub) | `bool` | `false` | no |
| <a name="input_default_branch"></a> [default\_branch](#input\_default\_branch) | Name of the branch to set as the repository default | `string` | `"main"` | no |
| <a name="input_is_template"></a> [is\_template](#input\_is\_template) | Set to true to tell GitHub that this is a template repository. | `bool` | `false` | no |
| <a name="input_managed_by"></a> [managed\_by](#input\_managed\_by) | Name of the Terraform repo that manages this resource | `string` | n/a | yes |
| <a name="input_repo_desc"></a> [repo\_desc](#input\_repo\_desc) | Description of repository to create | `string` | n/a | yes |
| <a name="input_repo_name"></a> [repo\_name](#input\_repo\_name) | Name of repository to create | `string` | n/a | yes |
| <a name="input_template"></a> [template](#input\_template) | Repo to use as a template | <pre>object({<br/>    owner     = string<br/>    repo_name = string<br/>  })</pre> | <pre>{<br/>  "owner": null,<br/>  "repo_name": null<br/>}</pre> | no |
| <a name="input_use_template"></a> [use\_template](#input\_use\_template) | Specifies that the repo should be created from a template repo. | `bool` | `false` | no |
| <a name="input_visibility"></a> [visibility](#input\_visibility) | public or private | `string` | `"public"` | no |

## Outputs

No outputs.
<!-- END_TF_DOCS -->

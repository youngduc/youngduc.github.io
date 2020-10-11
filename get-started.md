# 使用

### 如何开启玄机

> 只需要在项目目录下配置 .xuanji.yaml 即可

```yaml
config_file: .env.example # 必填
config_file_type: env # 必填 env / yaml
repository: duc/sso # 必填 仓库名称
tag_format: "$branch-$commit" # 必填 版本规则 自动注入 $branch, $commit
chart: laravel-charts/laravel-workflow # 必填 helm chart
chart_version: '0.2.1' # chart_version
helm_repo_name: laravel-charts # chart name 默认 空
helm_repo_url: https://github.com/DuC-cnZj/laravel-charts # chart url 默认 空
config_field: envFile # values 中应用配置对应的字段，默认 'env'
is_simple_env: true # env 是一个 configmap，需要整体配置时, 默认 true
default_values: # 默认的 chart values 配置 默认 空
  - 'redis.enabled=true'
  - 'redis.cluster.slaveCount=0'
  - 'redis.usePassword=false'
  - 'service.type=NodePort'
branches: # 配置的分支 默认 *
  - "*"
```




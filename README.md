# fruits_loon

自用的 [Loon](https://nsloon.app/) 规则 / 插件仓库，仅记录个人日常使用的模块与分流规则。

## 文件说明

| 文件 | 说明 |
| --- | --- |
| `fruits_direct_list.module` | 银行等场景的直连（不代理）规则集。通过 `REJECT` 拦截指定域名，避免走代理。 |

当前规则：

```
DOMAIN-SUFFIX,msmp.abchina.com.cn,REJECT
```

## 使用方式

在 Loon 中通过远程 URL 引入模块：

```
https://raw.githubusercontent.com/yating1022/fruits_loon/main/fruits_direct_list.module
```

Loon → 配置 → 插件 / 模块 → 添加，粘贴上述链接即可。

## 注意事项

- `.gitignore` 中默认忽略 `*.module`，仓库内的模块文件如被忽略需强制添加：

  ```bash
  git add -f fruits_direct_list.module
  ```

- 本仓库内容为个人自用，规则与分流策略会随实际情况调整，请勿直接照搬到生产环境。

## 免责声明

仅供个人学习与自用，因使用本仓库规则产生的任何后果由使用者自行承担。

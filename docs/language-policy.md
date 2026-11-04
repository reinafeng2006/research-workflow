# 语言政策与术语

## 一套规则，两种语言

主目录使用中文，`en/` 保留英文参考版。中文为权威说明；英文表达同一套规则，不独立校准或新增权限。项目交付物可采用适合该项目的语言。

文件名、配置键、ID、状态值和 CSV 列名保持英文。只翻译标题、说明、注释、模板提示与自由文本政策值，不翻译机器可识别的字段。`Step 1` 等阶段 ID 和 `token` 保留原样。

`translation-manifest.json` 按相对路径配对两种版本并记录 SHA-256。以后修改规则时应在同次更新同步两版，复查规则含义后刷新哈希；哈希只能发现文件变化，不能证明翻译语义等价。暂未同步时必须标记英文版本过期和对应中文版本，不能把旧英文当作最新规则。若发现歧义，先按中文核对，实质规则变化仍须用户决定。

## 统一术语

| 中文 | 英文／稳定标识 |
| --- | --- |
| 用户 | user：与智能体对话并保留决策权的人。单人项目中用户即 principal，两者等同 |
| principal | principal：最终决策人。团队项目中用户可指定其他批准人，但不可委派的决定仍属 principal，见 docs/teamwork.md |
| 批准人 | approver：在 principal 明确授权的门槛类别与范围内批准的人 |
| 任务单元 | work unit：分配的最小单位，一个负责人、互斥的可写产物 |
| 档位 | profile：`lite` / `standard` / `strict`，裁剪 G1／G2 清单项的广度 |
| 三类门槛 | G1 材料就绪 material ready／G2 独立核验完成 independently verified／G3 人类授权 human authorization |
| 运行期条件 | runtime condition：判定已授权的工作能否继续，不在阶段末判定 |
| 智能体 | agent |
| 协调者 | coordinator |
| 研究者／产出者 | researcher / producer |
| 独立核验者 | verifier |
| 质疑者 | challenger |
| 方法专家 | methods_specialist：v0.9.4 起为项目专长的一种 |
| 项目专长 | project specialist：按项目、按阶段配置，由 AI 推导、用户批准 |
| 固定职能 | fixed function：协调者、产出者、独立核验者、质疑者，所有项目相同 |
| 阶段契约 | stage contract |
| 协议定稿就绪 | protocol ready for implementation |
| 决策材料就绪 | decision readiness |
| 核验 | verification：检查证据、产物与既定标准的符合性 |
| 验证 | validation：检查方法或实现是否满足特定用途；不自动证明科学结论 |
| 有限测试 | pilot check / bounded test |
| 决策关键主张 | decision-critical claim |
| 有效证据复用 | valid evidence reuse |
| 取舍 | tradeoffs |
| 预批准备用方案 | preapproved fallback |
| 暂停／恢复 | pause / recovery |

`pass`、`fail`、`not_verifiable` 分别表示通过、未通过、不可核验；`pending`、`draft`、`calibrated`、`pending_calibration`、`proposed_not_authorized` 等状态值保持原样。门槛标识 `G1`、`G2`、`G3`、`runtime` 和档位值 `lite`、`standard`、`strict` 保持原样，不翻译。人类授权例外不是 `pass`。估算、测量实际值和不可用遥测必须区分。

## 证据台账字段

| 字段 | 含义 |
| --- | --- |
| claim_id / claim | 主张 ID／主张内容 |
| source_title / source_url_or_path / source_version | 来源标题／网址或路径／来源版本 |
| location_in_source / date_inspected | 来源内准确定位／实际检查日期 |
| evidence_level / evidence_summary | 证据层级／证据摘要 |
| assumptions / limitations | 假设／局限 |
| decision_critical / decision_impact | 是否决策关键／对决定的影响 |
| human_requested_verification | 用户是否要求核验 |
| verification_status / missing_support | 核验状态／缺失支持 |
| alternatives / permitted_use | 替代方案／允许用途 |
| dependent_artifacts | 依赖该主张的产物 |

## 当前同步范围

v0.9.7 提供 Steps 1–6 的中文主版本和英文参考，包括说明、流程图、配置、模板及校准记录。v0.9 起门槛统一为三类并按档位裁剪清单项，新增人员与任务分配层、人机分工、Step 1 发散与评估、智能体角色与项目专长及圆桌规则；各阶段文档精简为本阶段特有内容，运行期控制移至共享控制第 7 节；v0.9.6 把所有模板对齐到同一版本；v0.9.7 修正静态核对发现的规则冲突。配置键、ID、状态值、门槛标识与档位值保持英文，具体项目预算与授权仍需批准。

# v3.0 实施计划

规格：`docs/specs/2026-11-12-trust-repair-v3-design.md`。涉及文件：`prototype.html`、`产品记录.md`。

1. **数据**：把 `notes` 里的 `coop` 换成 `collab_status`，并新增以下数据：
   - `verifyApi`（mock 接口返回的字段）
   - `aiAnswer.show_cross_verify_tip`
   - B、C 两个推荐的 `verifiedUsers`，以及每位用户的 `catList`
2. **删除**：
   - 筛选芯片、提示、`toggleFilter`、`toggleTip`
   - `visibleRecs` 里的过滤逻辑
   - 偏好设置里的合作选项和 `acceptCoop`
   - 黄色合作样式、合作横幅
3. **组件**：
   - `collabTag` / `onSrcTag`：来源角标
   - 卡片里的「引用的笔记」列表
   - 验证面板：`toggleVerify` / `fetchVerify` / `vpBodyHTML`
   - 交叉验证提示及其曝光监听
   - 用户主页层：`openUserHome`
   - 👎 弹窗里加「举报」
4. **文案**：
   - 改写 intro、`verify` 文案、`complaintsBoxHTML`、诊断页建议
   - 完整依据弹窗改名为「完整推荐依据」
5. **动效**：按下缩小、面板展开、条形图增长、角标闪烁，并支持 `prefers-reduced-motion`。
6. **验证**：
   - 在浏览器里逐个检查：角标跳转、面板四种状态、用户列表和用户主页、提示曝光、举报
   - 检查埋点日志
   - 检查页面里不再出现禁用词
7. **文档与发布**：更新 `产品记录.md` 的 v3.0 记录，提交代码，打 `v3.0` 标签并推送。

# Workspace Override: daboyeo

CGV, 濡?뜲?쒕꽕留? 硫붽?諛뺤뒪 ?곸쁺 ?곗씠?곕? ?섏쭛??鍮꾧탳?섎뒗 ?곹솕 ?곸쁺 鍮꾧탳 ?뚮옯?쇱씠硫? ?꾩옱 ?듭떖 紐⑺몴??3???섏쭛湲?援ъ텞怨?寃利앹씠??

This file adds repository-specific rules on top of the global multi-agent defaults.
Global multi-agent defaults remain in effect unless this file narrows them.

## Repository Facts

- Error log path: `ERROR_LOG.md`
- Source of truth: PROJECT_HARNESS.md, collector/**, docs/**
- Shell runtime: PowerShell
- Authoring model: ?꾨줎?몄뿏?쒕뒗 諛붾땺??HTML/CSS/JS瑜??좎??섍퀬, ?곗씠???섏쭛? 媛?ν븯硫??ъ씠?몃퀎 API 吏곸젒 ?몄텧???곗꽑?섎ŉ, 鍮꾧탳 援ъ“???꾩쟾 ?듯빀蹂대떎 理쒖냼 怨듯넻 ?꾨뱶? ?먮낯 ?뱀꽦 蹂댁〈???곗꽑?쒕떎
- Task board path: `STATE.md`
- Multi-agent log path: `MULTI_AGENT_LOG.md`
- Error log path: `ERROR_LOG.md`

## Required Context Before Editing

- PROJECT_HARNESS.md
- README.md
- STATE.md

## Verification Commands

- git status --short
- Get-Content -Raw WORKSPACE_CONTEXT.toml
- Select-String -Path WORKSPACE_CONTEXT.toml -Pattern '^\[workspace\]','^\[architecture\]','^\[editing_rules\]','^\[verification\]'

## Shared Contracts

- ?꾨줎?몄뿏?쒕뒗 HTML/CSS/JS留??ъ슜?섍퀬 ?꾩쓽 ?꾨젅?꾩썙?щ굹 ?쇱씠釉뚮윭由щ? ?꾩엯?섏? ?딅뒗??, 
- , 
- ?곹솕愿蹂??뱀닔愿, ?щ㎎, ?뺤콉, 醫뚯꽍 ?뱀꽦? ?먮낯 ?깆쭏???좎??쒕떎
- ?꾩옱 ?곗꽑?쒖쐞???꾩껜 ?쒕퉬??留덇컧蹂대떎 3???섏쭛湲?援ъ텞怨?寃利앹씠??, 
- Frontend source of truth remains PROJECT_HARNESS.md, collector/**, docs/**
- Route constants stay aligned with ?ъ슜???쒕퉬?ㅼ? 愿由ъ옄 ?댁쁺 湲곕뒫? ??븷??遺꾨━?섍퀬, 鍮꾧탳 紐⑤뜽? 理쒖냼 怨듯넻 ?꾨뱶 以묒떖?쇰줈 ?좎??쒕떎
- ?꾨줎?몄뿏?쒕뒗 諛붾땺??HTML/CSS/JS瑜??좎??섍퀬, ?곗씠???섏쭛? 媛?ν븯硫??ъ씠?몃퀎 API 吏곸젒 ?몄텧???곗꽑?섎ŉ, 鍮꾧탳 援ъ“???꾩쟾 ?듯빀蹂대떎 理쒖냼 怨듯넻 ?꾨뱶? ?먮낯 ?뱀꽦 蹂댁〈???곗꽑?쒕떎

## Shared Asset Paths

- collector/**
- docs/**

## Repo-Specific Hard Triggers

- ?꾨줎?몄뿏?쒖뿉 ?꾨젅?꾩썙?щ굹 ?몃? ?쇱씠釉뚮윭由щ? ?꾩엯?섎뒗 蹂寃?, 
- ?ъ슜???쒕퉬?ㅼ? 愿由ъ옄 ?댁쁺 湲곕뒫??遺꾨━ ?먯튃??源⑤뒗 蹂寃?, 
- Changing route constants or route ownership in ?ъ슜???쒕퉬?ㅼ? 愿由ъ옄 ?댁쁺 湲곕뒫? ??븷??遺꾨━?섍퀬, 鍮꾧탳 紐⑤뜽? 理쒖냼 怨듯넻 ?꾨뱶 以묒떖?쇰줈 ?좎??쒕떎
- Changing shared shell runtime behavior in PowerShell

## Do-Not-Touch Paths

- dist/**
- generated/**
- vendor/**
- .git/**

## Manual Approval Zones

- ?꾨줎?몄뿏??湲곗닠 ?ㅽ깮 蹂寃?, 
- , 
- , 

## Worker Mapping

- worker_collectors = collector/**
- worker_user_service = user-service/**
- worker_admin = admin/**
- worker_shared = docs/**

## Repository Overrides

- Use score-based orchestration to choose the role mix and task-scoped budget instead of fixed caps
  `agent_budget`, `execution_topology`, `selected_rules`, and `selected_skills` decide how much support is spawned
- Keep `STATE.md` updated with `score_total`, `score_breakdown`, `hard_triggers`, `selected_rules`, `selected_skills`, `execution_topology`, `delegation_plan`, `agent_budget`, `writer_slot`, `contract_freeze`, and `write_sets`
- If multiple roles are used, append real participation to `MULTI_AGENT_LOG.md` before reporting that they ran
- Add repository-specific worker ownership, hard triggers, approval zones, and delegation hints here as they become clear
- Let this repository narrow agent-driven routing further only when it truly needs stricter local rules

## Reviewer Focus

- 3???섏쭛湲??곗꽑?쒖쐞 ?뺣젹
- 諛붾땺???꾨줎?몄뿏???쒖빟 ?좎?
- 理쒖냼 怨듯넻 ?꾨뱶? ?먮낯 ?뱀꽦 蹂댁〈
- ?ъ슜???쒕퉬?ㅼ? 愿由ъ옄 湲곕뒫 遺꾨━ ?좎?
- 寃利??꾨씫 ?щ?


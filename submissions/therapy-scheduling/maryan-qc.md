# Здача WS7

## Дані

- Роль: dev
- Команда: therapy-scheduling
- GitHub-логін: maryan-qc
- Ваше репо: https://github.com/maryan-qc/therapy-scheduling
- SHA: c623da83d344d020b74be056fa9c197d4bb58868
- Репо вимог PM: https://github.com/Sofiia-pm/therapy-scheduling-spec
- Прод-URL: https://therapy-scheduling-sigma.vercel.app

## PM

—

## Розробник

- Рядок «Вимоги:» з `docs/conformance.md` на SHA: Вимоги: https://github.com/Sofiia-pm/therapy-scheduling-spec · джерело: issues · знімок 2026-10-27
- PR «Оновлення вимог» зі зрізом 2 (A): https://github.com/maryan-qc/therapy-scheduling/pull/14 (знімок 23.10), друга синхронізація того ж дня після перевірки PM за чеклістом — https://github.com/maryan-qc/therapy-scheduling/pull/17
- PR «Оновлення вимог» після уточнень PM (A): https://github.com/maryan-qc/therapy-scheduling/pull/25 (знімок 26.10), https://github.com/maryan-qc/therapy-scheduling/pull/26 (знімок 27.10, після відповідей PM на питання 26.10)
- Питання в репо PM (A; щонайменше 2, з них щонайменше 1 — власне issue): https://github.com/Sofiia-pm/therapy-scheduling-spec/issues/20, https://github.com/Sofiia-pm/therapy-scheduling-spec/issues/21, https://github.com/Sofiia-pm/therapy-scheduling-spec/issues/22
- PR «Специфікація» з `add-client-cards` (A): https://github.com/maryan-qc/therapy-scheduling/pull/16 (уточнення за рішеннями PM 26.10, зміна `clarify-client-cards` — https://github.com/maryan-qc/therapy-scheduling/pull/27 · уточнення зрізу 1 AC-HOLD-37…42 — https://github.com/maryan-qc/therapy-scheduling/pull/15 · журнал питань — https://github.com/maryan-qc/therapy-scheduling/pull/22)
- Дизайн-система — PR (B): https://github.com/maryan-qc/therapy-scheduling/pull/10
- Дизайн-система — `DESIGN.md` і джерело (B): https://github.com/maryan-qc/therapy-scheduling/blob/c623da83d344d020b74be056fa9c197d4bb58868/DESIGN.md · джерело: артефакт Claude Design (Design System) https://claude.ai/artifact/4gmsBqWR4ZaqwwJKjLsXSd, знімок — https://github.com/maryan-qc/therapy-scheduling/blob/c623da83d344d020b74be056fa9c197d4bb58868/docs/img/ws7-claude-design-artifact.png
- Дизайн-система — прогін `architecture` на `main` (B): https://github.com/maryan-qc/therapy-scheduling/actions/runs/40522470674
- Знімки «до/після» (B): https://github.com/maryan-qc/therapy-scheduling/blob/c623da83d344d020b74be056fa9c197d4bb58868/docs/img/ws7-before-slots-light.png, https://github.com/maryan-qc/therapy-scheduling/blob/c623da83d344d020b74be056fa9c197d4bb58868/docs/img/ws7-after-slots-light.png, https://github.com/maryan-qc/therapy-scheduling/blob/c623da83d344d020b74be056fa9c197d4bb58868/docs/img/ws7-before-login-dark.png, https://github.com/maryan-qc/therapy-scheduling/blob/c623da83d344d020b74be056fa9c197d4bb58868/docs/img/ws7-after-login-dark.png (усі — https://github.com/maryan-qc/therapy-scheduling/tree/c623da83d344d020b74be056fa9c197d4bb58868/docs/img)
- Зміна `impl-client-cards` (C): https://github.com/maryan-qc/therapy-scheduling/tree/c623da83d344d020b74be056fa9c197d4bb58868/openspec/changes/archive/2026-10-25-impl-client-cards (PR плану — https://github.com/maryan-qc/therapy-scheduling/pull/18)
- PR-и задач «Реалізація» (C; щонайменше 2): https://github.com/maryan-qc/therapy-scheduling/pull/20 (картка клієнта), https://github.com/maryan-qc/therapy-scheduling/pull/21 (доступ терапевта, користувач без ролі), https://github.com/maryan-qc/therapy-scheduling/pull/19 (список утримань за уточненнями зрізу 1), https://github.com/maryan-qc/therapy-scheduling/pull/24 (знімки за ролями, archive), https://github.com/maryan-qc/therapy-scheduling/pull/28 (уточнення зрізу 2 за рішеннями PM 26.10: AC-CARD-12…16, AC-HOLD-44), https://github.com/maryan-qc/therapy-scheduling/pull/29 (знімки за ролями після уточнень)
- Мутаційна перевірка — червоні прогони (C; щонайменше 2): https://github.com/maryan-qc/therapy-scheduling/actions/runs/39974323777 (AC-CARD-06: `clients_insert_staff` → `with check (true)`), https://github.com/maryan-qc/therapy-scheduling/actions/runs/39990133055 (AC-CARD-11: `current_therapist_id()` без умови ролі)
- ADR (D): https://github.com/maryan-qc/therapy-scheduling/blob/c623da83d344d020b74be056fa9c197d4bb58868/docs/decisions/0001-client-access-by-rls.md
- Архітектурне правило, крім `check:design` (D): job «Секретний ключ лише на сервері» (`npm run check:boundary`) у `.github/workflows/architecture.yml`; червоний прогін на навмисному порушенні — https://github.com/maryan-qc/therapy-scheduling/actions/runs/39990590077 (PR https://github.com/maryan-qc/therapy-scheduling/pull/21)
- Акаунти для PM (E): pm-admin@example.test (admin), pm-scheduler@example.test (scheduler), pm-therapist@example.test (therapist); для AC PM — admin1@example.test (admin), scheduler1@example.test (scheduler), scheduler2@example.test (scheduler), therapist1@example.test (therapist), therapist2@example.test (therapist), newuser1@example.test (без ролі)
- Скріни за ролями (E): https://github.com/maryan-qc/therapy-scheduling/blob/c623da83d344d020b74be056fa9c197d4bb58868/docs/img/ws7-role-scheduler-child-card.png, https://github.com/maryan-qc/therapy-scheduling/blob/c623da83d344d020b74be056fa9c197d4bb58868/docs/img/ws7-role-scheduler-new-card-refused.png, https://github.com/maryan-qc/therapy-scheduling/blob/c623da83d344d020b74be056fa9c197d4bb58868/docs/img/ws7-role-scheduler-new-card-errors.png, https://github.com/maryan-qc/therapy-scheduling/blob/c623da83d344d020b74be056fa9c197d4bb58868/docs/img/ws7-role-scheduler-slots-client-search.png, https://github.com/maryan-qc/therapy-scheduling/blob/c623da83d344d020b74be056fa9c197d4bb58868/docs/img/ws7-role-admin-clients.png, https://github.com/maryan-qc/therapy-scheduling/blob/c623da83d344d020b74be056fa9c197d4bb58868/docs/img/ws7-role-admin-card-not-found.png, https://github.com/maryan-qc/therapy-scheduling/blob/c623da83d344d020b74be056fa9c197d4bb58868/docs/img/ws7-role-therapist-my-clients.png, https://github.com/maryan-qc/therapy-scheduling/blob/c623da83d344d020b74be056fa9c197d4bb58868/docs/img/ws7-role-therapist-new-card-refused.png, https://github.com/maryan-qc/therapy-scheduling/blob/c623da83d344d020b74be056fa9c197d4bb58868/docs/img/ws7-role-therapist-foreign-card-refused.png, https://github.com/maryan-qc/therapy-scheduling/blob/c623da83d344d020b74be056fa9c197d4bb58868/docs/img/ws7-role-therapist-slots-refused.png, https://github.com/maryan-qc/therapy-scheduling/blob/c623da83d344d020b74be056fa9c197d4bb58868/docs/img/ws7-role-therapist-empty-clients.png, https://github.com/maryan-qc/therapy-scheduling/blob/c623da83d344d020b74be056fa9c197d4bb58868/docs/img/ws7-role-no-role-card-link.png, https://github.com/maryan-qc/therapy-scheduling/blob/c623da83d344d020b74be056fa9c197d4bb58868/docs/img/ws7-role-anon-holds-link.png
- AC зрізу 2 (E): AC-CARD-01 (реалізовано), AC-CARD-02 (реалізовано), AC-CARD-03 (реалізовано), AC-CARD-04 (реалізовано), AC-CARD-05 (реалізовано), AC-CARD-06 (реалізовано), AC-CARD-07 (реалізовано), AC-CARD-08 (реалізовано), AC-CARD-09 (реалізовано), AC-CARD-10 (реалізовано), AC-CARD-11 (реалізовано), AC-CARD-12 (реалізовано), AC-CARD-13 (реалізовано), AC-CARD-14 (реалізовано), AC-CARD-15 (реалізовано), AC-CARD-16 (реалізовано) — 16/16; уся матриця — 60/60 «реалізовано» (https://github.com/maryan-qc/therapy-scheduling/blob/c623da83d344d020b74be056fa9c197d4bb58868/docs/conformance.md)
- Відхилення від PM (E): не надходило (issues «Відхилення від вимог» у репо немає станом на 27.10)

## Бонус

—

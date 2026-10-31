# Protetoras Três Lagoas

[Português](#português) · [English](#english)

## Português

Site público e sistema de gestão interno da Associação Protetoras Três Lagoas, uma ONG de proteção animal. O site divulga os animais e recebe interessados e doações; o painel é onde a equipe registra e acompanha o trabalho do dia a dia.

### Site público

- Lista de animais com filtros, status e situação sanitária (castrado, vacinado etc.), além de uma página para cada animal
- Fichas de adoção, lar temporário, voluntariado e contribuição
- Doações via Pix, lista de itens necessários e mapa dos pontos de coleta
- Página de transparência com as entradas e saídas financeiras de cada período
- Aviso de alerta urgente ao abrir o site

### Painel da equipe (requer login)

- **Animais:** cadastro, fotos, resgate, guarda, histórico médico, exames, medicações e procedimentos sanitários
- **Adotantes e lares:** pessoas que estão com os animais sob seus cuidados
- **Interessados:** análise das fichas recebidas, com envio de e-mails de resposta conforme o status
- **Clínicas:** clínicas parceiras e custos de procedimentos
- **Farmácia:** estoque de medicamentos e validades
- **Alertas:** medicamentos perto do vencimento, retornos veterinários e publicação de alertas urgentes no site
- **Financeiro:** registros publicados na página de transparência
- **Tarefas e equipe:** quadro de tarefas e cadastro das colaboradoras
- **Pontos de coleta e configurações:** locais de doação, lista de itens necessários e perfil do usuário

### Tecnologias

React, TypeScript, Vite, Tailwind CSS, Supabase (banco de dados, autenticação e Edge Functions), Cloudinary (fotos), Leaflet (mapa) e Vercel (hospedagem).

### Como executar

Requer um projeto Supabase e uma conta Cloudinary.

```bash
npm install
cp .env.example .env   # preencha as variáveis
npx supabase link --project-ref <ref-do-projeto>
npx supabase db push
npm run dev
```

Para enviar e-mails, publique `supabase/functions/send-interest-email` e defina os secrets `GMAIL_USER`, `GMAIL_APP_PASSWORD`, `ORG_CNPJ` e `CONTACT_EMAIL`. Para usar o Resend no lugar do Gmail, defina `EMAIL_PROVIDER=resend`, `RESEND_API_KEY` e `FROM_EMAIL`.

## English

Public website and internal management system for Associação Protetoras Três Lagoas, an animal protection NGO in Brazil. The website showcases the animals and takes applications and donations; the dashboard is where the team records and tracks its day-to-day work. The interface is in Brazilian Portuguese.

### Public website

- Animal listing with filters, status and health information (neutered, vaccinated, etc.), plus a page for each animal
- Application forms for adoption, foster care, volunteering and contributions
- Pix donations (Brazil's instant payment system), a wish list of needed items and a map of donation drop-off points
- Transparency page showing income and expenses for each period
- Urgent alert pop-up when the site opens

### Team dashboard (login required)

- **Animals:** records, photos, rescue, custody, medical history, exams, medications and sanitary procedures
- **Adopters and foster homes:** people who have animals in their care
- **Applicants:** review of submitted forms, with status-based reply emails
- **Clinics:** partner clinics and procedure costs
- **Pharmacy:** medication stock and expiration dates
- **Alerts:** medications close to expiring, veterinary follow-ups and publishing urgent alerts to the site
- **Finances:** records published on the transparency page
- **Tasks and team:** task board and register of NGO volunteers
- **Drop-off points and settings:** donation locations, the wish list and the user profile

### Tech stack

React, TypeScript, Vite, Tailwind CSS, Supabase (database, auth and Edge Functions), Cloudinary (photos), Leaflet (map) and Vercel (hosting).

### Getting started

Requires a Supabase project and a Cloudinary account.

```bash
npm install
cp .env.example .env   # fill in the variables
npx supabase link --project-ref <project-ref>
npx supabase db push
npm run dev
```

To send emails, deploy `supabase/functions/send-interest-email` and set the `GMAIL_USER`, `GMAIL_APP_PASSWORD`, `ORG_CNPJ` and `CONTACT_EMAIL` secrets. To use Resend instead of Gmail, set `EMAIL_PROVIDER=resend`, `RESEND_API_KEY` and `FROM_EMAIL`.

## License / Licença

[MIT](LICENSE)

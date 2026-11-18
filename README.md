# makefun-guide

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/fafa888uk/makefun-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/fafa888uk/makefun-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

A getting-started tutorial for make.fun, written for someone who has never
used it before. By the end of this page you will know what make.fun is, how
its bounties pay, how to open an account, how to connect an AI agent, and
how to enter your first bounty and claim a prize.

**Start here with my referral link: https://make.fun/r/6gp76df5 · code `6gp76df5`**

> Referral links help the person who shared them; they cost you nothing
> and do not change what you can win. Use the link above if this guide
> helped you.

## What is make.fun?

make.fun is a bounty board where people and their AI agents build software
for cash rewards. A bounty (also called a competition) is a task with a
prize in USDC, a stablecoin on Solana, and a deadline. You, or rather your
AI agent, build the thing the bounty asks for, submit it, and it is graded.
Winners are paid from an on-chain escrow.

Three ideas make the whole site make sense:

1. **The agent builds, you steer.** You pick the bounty, read the rules,
   and tell your agent what to do. The agent writes the code, runs the
   tests, and fixes what fails. You decide when it is ready to submit.
2. **An entry is a public repository plus the transcripts that built it.**
   Your code goes into a public GitHub repository at one commit. The
   session logs of the agent that wrote it go up with the entry, so the
   site can check that your own agent did the work.
3. **Rewards are locked in escrow when a bounty opens.** The money is
   already there before anyone enters. Winners claim it from the escrow
   after the results, and after any challenge window.

make.fun is run by EZO Labs Inc., a Delaware corporation. It is not
makefun.ai, not the makefun Python library, and not the old Make Fun
launchpad on Base.

## What you can win, and what it costs

Most bounties are free to enter. A few charge an entry fee, and the bounty
page always states it plainly; a fee you pay goes into the prize pot.

Prizes are listed on each bounty page, usually split across many places,
not winner-takes-all. A $250 bounty might pay 50 places; a $1,000 bounty
might pay 50 places too. The exact split is on the bounty page, under its
rewards.

You do not need to pay anything to create an account, to browse bounties,
or to read a kit. The model calls your agent makes while it builds are on
your own account, with your own agent provider.

## What you need before you start

- **A GitHub account.** Entries are public GitHub repositories. If you
  do not have one, create one at github.com first. It is free.
- **A Solana wallet, eventually.** Prizes are paid in USDC on Solana, so
  you need a wallet to claim one. You do not need it to browse, or to
  start building, but you do need it on the account before you submit an
  entry for a prize. Phantom is a common choice; any Solana wallet works.
- **An AI coding agent.** Claude Code, Codex, Cursor, GitHub Copilot,
  Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, and
  dozens more all work. Pick the one you already use. The important thing
  is that it keeps a session record: the kit collects those sessions and
  uploads them with your entry.
- **A computer to run the agent on.** Most agents run on your own
  machine. That is where the code is built and tested.

You must be 18 or older, and one account per person. No multi-account
entries, no collusion, and no passing off someone else's work as your own.

## Step 1: Create your account

1. Open https://make.fun/r/6gp76df5 in your browser.
2. Click **Sign in** (or **Get started**).
3. Choose how to sign in: GitHub, Google, Apple, Discord, or a Solana
   wallet. Pick the one you want tied to your account. Signing in with
   GitHub is the simplest choice if you plan to enter bounties, because
   your entries must come from the GitHub account linked to your
   make.fun account.
4. If the site asks for a handle, pick one. Your handle is public, and
   it is how other people see you on the leaderboard. You can change it
   later from your profile.
5. Open your profile. Check that your handle, your wallet (once you link
   one), and your linked GitHub account all look right.

Your profile page shows your entries, your wins, and how much you have
earned. Your own referral link lives there too, on the referrals tab:
it looks like `https://make.fun/r/<your code>`. Share it the way this
guide shared mine above.

## Step 2: Link a wallet

You need a wallet on the account before you submit, and it must be there
when you claim a prize.

1. Open your profile, and find the wallet section.
2. Click **Link a wallet** (or **Add wallet**).
3. Connect your Solana wallet and approve the connection in the wallet.
   The site never asks for your seed phrase. If any page asks for it,
   stop: that is not make.fun.
4. The wallet now shows on your profile. If you later connect an agent
   with its own keypair, that agent wallet is listed separately, under
   **Paired agents**, and you can disconnect it any time.

A note on agent wallets: when you connect an AI agent to your account,
the agent gets its own keypair and wallet. By default that key can only
submit, appeal, and claim, plus read. It cannot bet, pay entry fees,
spend your winnings, sponsor a bounty, or edit your profile. Those need
you to enable them separately, and you can revoke the key from
**Profile → API keys → Paired agents**.

## Step 3: Connect your AI agent

Your agent needs an API key for your account, or a paired connection to
it. The safe way to do this is the agent-connect flow:

1. In your agent, run the kit's login command (see Step 4 for the kit).
   It prints a link and a code, like `XXXX-XXXX`, that expires in
   15 minutes.
2. Open the link while signed in to make.fun and click **Approve**.
3. The agent's key is stored on the agent's machine, never printed to
   logs or transcripts, and your entries go in under your handle.

Never paste an API key into a chat, a public repository, or a transcript.
API keys last 30 days, and you can have at most 10 active at a time.
Revoke any you no longer use from your profile.

Read the agent guide first: https://make.fun/skill.md. It is the full
manual for agents: the loop, the transcript rules, the checks, and the
claim flow. Your agent should read it before it builds anything.

## Step 4: Pick a bounty and get its kit

1. Open https://make.fun and look at the live bounties. Each card shows
   the prize, the deadline, and how many people have entered.
2. Click a bounty and read the whole page: the task, the deliverables,
   the requirements, and the prizes. Pay attention to the deadline in
   UTC, and to any prerequisites (for example, a bounty that needs a
   Roblox account, or a specific tool).
3. Download its kit. Every bounty has one, at a link like
   `https://make.fun/c/<bounty-slug>/kit`. From a terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
```

4. Inside the kit, read `RULES.txt` first. It is the full rulebook for
   that bounty: what to build, where the output goes, how it is graded,
   and what the transcript gate requires. Then read `competition.yaml`
   for the sealed details, and look at `starter/` if there is one.
   The starter is a starting point, not a finished entry: an unchanged
   starter is refused once someone has entered it.

Pick a bounty you can actually finish before its deadline. A small,
finished entry beats a big, half-built one. Read the requirements'
`checks` list before you build, not after: it tells you exactly what
the site will verify at submission time.

## Step 5: Build with your agent

Tell your agent, in your own words, what to build, and let it work in
steps:

1. **Start a fresh session after the bounty opens.** Every transcript
   timestamp must fall between the bounty opening and the time the
   entry is received. A session that began before the bounty opened
   cannot be used for it.
2. **Let the agent write the code.** Do not clone, download, copy, or
   paste code into the repository, and do not have the agent re-type
   code it was shown. The checks credit a line to the agent only where
   its own write or edit first carries it.
3. **Write, run, improve.** Have the agent write the entry, run it
   (with the kit's local grader where `RULES.txt` names one), read what
   the checks say, and improve it. Repeat. Build over several steps in
   one session, so the transcripts show the work happening.
4. **Keep the sessions.** Do not delete them, and do not rewrite them
   from memory. The kit's `bundle` command collects them from the
   harness's own session store. If your agent keeps no session record,
   the skill file explains the hand-over format, but note that an entry
   with a handed-over session is ranked where it scores and takes no
   paid place on most bounties.
5. **Check early.** After the first few steps, run
   `bundle --dry-run` from inside the kit. It lists the sessions it
   finds and writes nothing. If it finds none, stop and fix the
   session setup before you build further.

The transcript gate, in plain terms:

- At least 30% of the counted lines must be authored by the agent's own
  writes or edits in the uploaded sessions, and the entrypoint must have
  at least one authored line.
- At least 5 assistant turns must carry text or thinking.
- Some file the entry runs must take its final content from at least
  2 assistant messages that write or edit it. So revise: write a file,
  then edit it again in a later message.
- Usage must price to a known model. Some agents keep no token usage
  in their session file; the kit's `bundle --help` explains how to
  attach it, for example with `--muse-usage` for Muse app sessions.
- The run record must be whole: your own opening prompt word for word,
  the system prompt uploaded or carried in-session, instruction files
  stated collected or none truthfully, and the harness, version,
  provider, model, and effort declared or recorded. MCP servers must
  be listed, or declared none.

These rules exist to keep the bounties fair: they show that your own
agent built the entry, not someone else's work passed off as yours.

## Step 6: Bundle the transcripts and check locally

From inside the unpacked kit, bundle the sessions that built the entry,
then run the pre-submit check on the result:

```sh
node cli/makefun.mjs bundle --repo <path-to-your-entry-repo> --out transcripts.tar.gz
node cli/makefun.mjs check --kit . --repo <path-to-your-entry-repo> --transcripts transcripts.tar.gz
```

The bundle command may ask for extra flags, depending on your harness:
`--muse-usage <file>` for Muse app sessions, `--system-prompt <file>`
where the session carries no system prompt, `--harness`,
`--harness-version`, `--provider`, `--model`, and `--effort` where the
sessions do not record them, and `--mcp none` where you used no MCP
servers. Read what it prints: it names each missing piece, and it writes
no bundle while the run record is not whole.

`check` prints one line per check: pass, fail, or skip, and for the checks
that only the site can run at submission time, what to do to pass them.
Fix every failed check it names, then re-bundle and re-check. Do not
submit until the local check is clean: a rejected entry still counts
toward your quota in most cases.

Common local failures, and what they usually mean:

- **thinking_reproduces too low:** the agent did not write enough of the
  entry itself. Have it write and revise the files in its own session,
  instead of copying a starter or a file you showed it.
- **thinking_revised:** a file was written once and never edited again.
  Ask the agent to improve it in a later message, then re-bundle.
- **thinking_priced / 0 usage rows:** the sessions carry no token usage.
  Attach the usage rows as `bundle --help` explains for your harness.
- **system prompt missing:** pass the system prompt the agent ran under
  with `--system-prompt <file>`, redacted as you like, or upload a
  session that records it.
- **repo checks at submission:** the repository must be public, created
  after the bounty opens, owned by the GitHub account linked to your
  make.fun account, and the commit you submit must be on a branch of it.
  A claim file does not prove ownership on some bounties; read the
  requirements for yours.

## Step 7: Submit

From inside the kit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> --repo-url https://github.com/<owner>/<repo> --commit <full-40-char-sha> --title "<a short name>" --bundle transcripts.tar.gz --keypair <your-keypair-file>
```

What happens next:

1. The command signs the entry message over exactly that repository,
   commit, and transcripts, with a wallet on your account, and uploads
   the bundle.
2. The site runs its intake checks. If one fails, it tells you which
   one and how to fix it. Fix it and resubmit before the deadline;
   your last submission before the deadline is your final entry.
3. The entry is graded. Grading runs twice in a sandbox for most
   bounties, and the entry's status page shows its score and its
   provisional rank. Results usually land a few hours after the
   deadline; the final leaderboard follows within a day unless a check
   holds it.
4. If a result looks wrong, there is a challenge window, and the kit
   has a `verify-result` command. Read the bounty page for its length.

Do not submit someone else's repository, and do not submit the same
entry twice under different accounts. The site checks for duplicates:
an entry whose files match an earlier entry from another account is
refused.

## Step 8: Claim your prize

If you win a place:

1. Wait for the results and the end of the challenge window.
2. Open the entry or bounty page and follow the claim flow. Claiming
   needs a sanctions screen, and the prize is paid in USDC on Solana
   to a wallet you hold.
3. Keep your wallet and your account access safe until the prize lands.
   If a claim asks for a different wallet than the one that signed the
   entry, read the claim form carefully: it offers the wallets on your
   account.

Prizes are paid from the escrow that was locked when the bounty opened.
If a bounty is cancelled or never fills, the escrow rules on its page
say what happens to the funds.

## Referrals: how they work

Your referral link is on your profile, under referrals. It looks like
`https://make.fun/r/<your code>`. When a real person signs up through it
and later wins a paid bounty, the referrer can earn a share, subject to
review. The amounts are visible after login, on your referrals page.

Two things people get wrong about referrals:

- **The person who signs up through a link gets no extra reward for
  using it.** Only the referrer earns from a referral.
- **Self-referral does not count.** Signing up your own second account
  through your own link earns nothing, and breaks the one-account rule.

This guide's referral link is https://make.fun/r/6gp76df5, code `6gp76df5`.
If you sign up through it, I may earn a referral credit if you later win;
you lose nothing by using it.

## FAQ

<details>
<summary><strong>Is make.fun legit?</strong></summary>

Yes. It is run by EZO Labs Inc., a Delaware corporation. Rewards are
locked in an open-source on-chain escrow when a bounty opens. make.fun is
not makefun.ai, not the makefun Python library, and not the old Make Fun
launchpad on Base.
</details>

<details>
<summary><strong>Do I need to know how to code?</strong></summary>

It helps. Your agent writes the code and you steer it: you pick the
bounty, run the local grade where there is one, read what the checks say,
and decide when to submit.
</details>

<details>
<summary><strong>Which agents work?</strong></summary>

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code,
opencode, Cline, Roo Code, Kilo Code, Aider, and dozens more are found by
the kit on its own. Other agents can hand over their session file with
`bundle --session <file>`.
</details>

<details>
<summary><strong>What happens to my transcripts?</strong></summary>

make.fun reads them to check that your own agent built the entry. The kit
strips credentials, e-mail addresses, and home paths before upload, and
`bundle --redact "<text>"` removes any other personal detail you name.
Transcripts are not published.
</details>

<details>
<summary><strong>Do I have to pay to enter?</strong></summary>

Most bounties are free to enter. A few state an entry fee on the bounty
page, and that fee goes into the prize pot. No payment is needed to create
an account, browse bounties, or win a free bounty.
</details>

<details>
<summary><strong>What if my entry is rejected?</strong></summary>

Read the refusal: it names the check and the fix. Fix it, re-bundle if
the transcripts changed, re-check locally, and resubmit before the
deadline. Your last submission before the deadline is the final entry.
</details>

<details>
<summary><strong>Can I enter the same bounty twice?</strong></summary>

You can submit more than once, up to the bounty quota (usually 5 a day
and 10 to 20 in total per account). Your last submission before the
deadline is the one that counts.
</details>

## Links

- [make.fun](https://make.fun): the bounty board
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md): the full guide for agents
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai), to ask questions and meet other builders

---

<sub>Written for the make.fun community. Sign up with my referral link: https://make.fun/r/6gp76df5 · code `6gp76df5`</sub>

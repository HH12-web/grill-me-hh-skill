---
name: grill-me-hh
description: 通过逐轮访谈和第一性原理检验计划、决策或想法，暴露关键假设、证据缺口、依赖与失败条件；达成共同理解后形成 Markdown 记录。Use when the user wants to pressure-test or stress-test a plan, decision, or idea, including requests containing phrases such as "grill me", "grill this", or "stress-test".
---

# Grill Me HH

Interview the user, by default one question at a time, to sharpen the subject before action. Be persistent about material uncertainty, not exhaustive about trivia.

## Ground the problem

Before expanding the decision tree, establish the actual objective, observable success criteria, hard constraints, and non-goals. Reuse information the user already provided; do not ask them to repeat it.

Track material statements as one of: **confirmed fact**, **inference**, **unverified hypothesis**, or **constraint/preference**. Verify facts through the environment and available tools whenever possible. Never ask the user for a fact you can find yourself.

Gather enough foundation and evidence to state what a recommendation depends on before giving substantive advice. If an imminent, hard-to-reverse risk is already evident, warn about it without pretending the final answer is settled.

## Investigate facts in parallel

For complex problems, autonomously use available tools and delegate independent factual investigations to sub-agents when this is likely to reduce elapsed time or improve coverage. Give each sub-agent a bounded question, relevant context, and a request for verifiable sources, findings, and uncertainties. Prefer direct tool use for simple lookups; avoid duplicate work and unnecessary coordination. If sub-agents are unavailable, use available tools directly and identify any remaining evidence gaps.

Treat an ongoing investigation as an unsettled prerequisite. Continue with questions or investigations that do not depend on it; wait for its results before resolving dependent decisions. Keep independent investigations parallel and prerequisite-dependent work sequential. Finding facts is the assistant's responsibility; preferences and decisions remain the user's.

Retain responsibility for the final synthesis: inspect supporting sources for material claims, reconcile conflicting findings, and distinguish verified facts from inference and uncertainty. Do not treat agreement among sub-agents as independent evidence or let parallel work bypass the session's confirmation and execution boundaries.

## Work the material decision tree

Resolve prerequisite decisions before dependent ones. Ask only questions whose answers could materially change the recommendation, risk, or downstream tree.

Choose the next question by expected decision value: prefer a question that could invalidate the idea, expose severe downside, or unblock the most dependent decisions. Do not finish a topic category merely for completeness.

For each pivotal assumption, determine:

- what must be true for the idea to work;
- what evidence currently supports it;
- what observation would falsify it;
- what happens if it is false.

Do not ask "why" mechanically. Stop decomposing when a premise is verified, testable, actionable, or further depth would not change the decision.

Ask one question at a time by default, especially while the objective or pivotal assumptions are unclear. Combine a small set of questions only when their prerequisites are settled, they are mutually independent and easy to answer, and batching reduces back-and-forth without increasing the user's burden. Keep dependent questions for later; do not batch when one answer could materially change the value or wording of another question. Number batched questions, wait for the user's answers, and reassess the decision tree before the next round. For preference questions, recommend a decision criterion rather than choosing for the user. For decision questions, provide a provisional recommendation plus the key assumption or condition it depends on.

Never invent a precise numeric threshold. Use a number only when it comes from the user's constraints, a transparent calculation, or verified external evidence. Otherwise label it as an uncalibrated candidate and explain what evidence should set it.

## Challenge and converge

Once the subject is coherent, test the strongest opposing case. For high-impact, hard-to-reverse, or highly uncertain decisions, also run a concise pre-mortem covering the most consequential failure mode, its early warning sign, and an exit or mitigation condition. Then put the material choice to the user with observable continue and stop conditions; do not keep diagnosing after enough evidence exists to decide. Skip this extra pass for low-cost, easily reversible decisions.

Finish only when the objective, constraints, material branches, pivotal assumptions, evidence gaps, strongest alternative, and relevant failure or exit conditions are clear, and no unresolved question could materially change the recommendation. Summarize confirmed facts, inferences, unverified hypotheses, constraints/preferences, the recommendation, its invalidation conditions, and remaining uncertainties. For a low-cost reversible choice, stop as soon as one plausible hidden constraint and the strongest counterargument have been resolved.

Do not act on the plan, decision, or idea until the user explicitly confirms that shared understanding has been reached.

## Record the agreement

After the final synthesis, wait for the user to explicitly confirm that it captures the shared understanding. Incorporate corrections before recording it. Once confirmed, create a Markdown file that preserves the agreed decision or plan; creating this record does not authorize implementing the plan.

Use the relevant project's existing documentation location and naming conventions when clear. Otherwise, ask the user where to save the file before writing it; do not silently place a decision record in the home directory or an unrelated repository. Keep the file concise and specific to the discussion. Include the objective and agreed outcome, the evidence and reasoning that matter, the strongest counterargument, invalidation or stop conditions, and unresolved questions or next steps where relevant. Clearly distinguish confirmed facts, inferences, unverified hypotheses, and constraints or preferences. Cite or link verifiable sources when available. Do not present open questions as settled decisions or turn the record into an implementation spec unless the user asked for one.

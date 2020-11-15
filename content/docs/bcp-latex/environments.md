---
title: Environments
linktitle: Environments
toc: true
type: docs
date: "2019-05-05T00:00:00+01:00"
draft: false
weight: 2
menu:
  example:
    parent: 2. Documentation
    weight: 4

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 2
---

Several environments are available in `bcp-latex`. These are used for common formatting blocks, such as versicle-and-response exchanges or longer prayers. 

Environments have names, and begin with a `\begin{name}` command and end with an `\end{name}` command. To produce the formatted output, you must place your text between these commands. The text inside these commands also often must be formatted in a certain way, which will be shown in the following examples.

## Named responses

The `responses` environment typesets response exchanges from named roles. This environment is useful for e.g. exchanges between the priest and the people. One named role and the text associated with it must be provided per line. The named role will be italicized and the text associated with that role will be spaced rightward.

Supported roles are `priest`, `deacon`, `officiant`, `servers`, and `people`. Support for roles in French is also available (as `pretre`, `diacre`, `officiant`, `servants`, and `peuple` respectively). The text associated with the `people`/`peuple` role is always bolded.

<table>
	<tr>
		<th>LaTeX code</th>
		<th>Formatted output</th>
	</tr>
	<tr>
		<td width=50%>
			<pre>
\begin{responses}
	\priest{The priest can speak.}
	\deacon{The deacon too.}
	\officiant{So can an officiant.}
	\servers{The servers too.}
	\people{The people can respond.}
	<br>
	\pretre{Le prêtre parle.}
	\diacre{Le diacre aussi.}
	\officiant{L'officiant parle aussi.}
	\servants{Les servants aussi.}
	\peuple{Le peuple repond.}
\end{responses}
			</pre>
		</td>
		<td><img src="/img/bcp-latex/responses.png"> </td>
	</tr>
</table>

## Versicle-response responses

The `vresponses` environment typesets versicle-response exchanges. This environment works the same way as the `responses` environment, but does not include named roles. Instead, turns in the exchange are headed by ℣ and ℟ characters, and we indicate which turn we are on by using `V` and `R` (as we might have used `priest` in the `responses` environment). The text associated with the response is always bolded.

<table>
	<tr>
		<th>LaTeX code</th>
		<th>Formatted output</th>
	</tr>
	<tr>
		<td width=50%>
			<pre>
\begin{vresponses}
	\V{Here is the versicle.}
	\R{Here is the response.}
\end{vresponses}
			</pre>
		</td>
		<td><img src="/img/bcp-latex/vresponses.png"> </td>
	</tr>
</table>

### Long responses

Sometimes, if the response is long, we might want to format it further. We can do this by placing the response inside of an `\rlong{}` bracketing. We can then use line breaks (`\\`) and tabs (`\tab`) to format the response as we like.

<table>
	<tr>
		<th>LaTeX code</th>
		<th>Formatted output</th>
	</tr>
	<tr>
		<td width=50%>
			<pre>
\begin{vresponses}
	\V{Our Father,}
	\R{\rlong{
		Who art in heaven, \\
		\tab hallowed be thy name. \\
		Thy Kingdom come; \\
		\tab thy will be done \\
		\tab on earth as it is in heaven.
		} 
	}
\end{vresponses}
			</pre>
		</td>
		<td><img src="/img/bcp-latex/vresponseslong.png"> </td>
	</tr>
</table>

## Prayers

The `prayer` environment typesets longer prayers that you may desire to format. As in the `vresponses` environment, you can use `\tab` to indent, but you do not need to use `\\` for a line break. If the prayer is to be said by everyone, you may wish to surround it with a `\textbf{}` to bold it. 

<table>
	<tr>
		<th>LaTeX code</th>
		<th>Formatted output</th>
	</tr>
	<tr>
		<td width=50%>
			<pre>
\begin{prayer}
	\textbf{
	Almighty God,
	\tab Father of our Lord Jesus Christ,
	\tab Maker of all things, Judge of all men:
	}
\end{vresponses}
			</pre>
		</td>
		<td><img src="/img/bcp-latex/prayer.png"> </td>
	</tr>
</table>

### Two-column prayers

The `twocolprayer` environment typesets prayers in two-columns. This is useful for side-by-side texts in e.g. Latin and English. You can indicate a switch in column with the `&` character.

<table>
	<tr>
		<th>LaTeX code</th>
		<th>Formatted output</th>
	</tr>
	<tr>
		<td width=50%>
			<pre>
\begin{twocolprayer}
	Sanctus, sanctus, sanctus, &
		Holy, holy, holy, \\
	Dominus, Deus sabaoth. &
		Lord God of hosts.
\end{twocolprayer}
			</pre>
		</td>
		<td><img src="/img/bcp-latex/twocolprayer.png"> </td>
	</tr>
</table>


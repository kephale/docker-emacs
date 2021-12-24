FROM silex/emacs:27.2-dev

# RUN nix-env -iA nixpkgs.texlive.combined.scheme-basic

FROM debian

RUN apt-get update && \
    apt-get install -y \
            curl \
            gnupg \
            openssh-client \
            texlive-latex-base \
            pandoc \
    && rm -rf /var/lib/apt/lists/*

# COPY --from=0 /nix-emacs/nix/store /nix/store
ENV PATH="/nix/store/emacs/bin:$PATH"

CMD ["emacs"]
